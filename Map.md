# Map
```
Map<String, String> nameMap = new Map<String,String>();
nameMap.put('Rakesh','Singh');
nameMap.put('Priyanka','Gupta');
nameMap.put('Pooja','Gupta');
nameMap.put('Utkarsh','Singh');
nameMap.put('Tanishka','Gupta');
System.debug('nameMap->'+nameMap);
```
# Access Keys and Values
```
Set<String> firstName = nameMap.keySet();
System.debug('firstName->'+firstName);
List<String> LastName = nameMap.values();
System.debug('LastName->'+LastName);
```
# Contains Key and Value
```
Boolean nameExist= nameMap.containsKey('Rakesh');
System.debug('nameExist->'+nameExist);
Boolean LastNameExistFromMap= nameMap.values().contains('Gupta');
System.debug('LastNameExistFromMap->'+nameExist);
Boolean LastNameExistFromList= LastName.contains('Gupta');
System.debug('LastNameExistFromList->'+nameExist);
```
