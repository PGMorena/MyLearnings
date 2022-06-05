# Map
```
Map<String, String> nameMap = new Map<String,String>();
nameMap.put('Rakesh','Singh');
nameMap.put('Priyanka','Gupta');
nameMap.put('Pooja','Gupta');
nameMap.put('Utkarsh','Singh');
nameMap.put('Tanishka','Gupta');
System.debug('nameMap->'+nameMap);
System.debug('Rakesh surname->'+nameMap.get('Rakesh'));
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
# Map of string and list of string
```
Map<String,List<String>> familyMap = new Map<String,List<String>>();
List<String> RakeshfamilyValue = new List<String>();
RakeshfamilyValue.add('Priyanka');
RakeshfamilyValue.add('Roushan');
List<String> PriyankafamilyValue = new List<String>();
PriyankafamilyValue.add('Udit');
PriyankafamilyValue.add('Utkarsh');
  
familyMap.put('Rakesh',RakeshfamilyValue);
familyMap.put('Priyanka',PriyankafamilyValue);
System.debug('familyMap->'+familyMap);
System.debug('Rakesh family->'+familyMap.get('Rakesh'));
Set<String> familyKey= familyMap.keySet();
System.debug('familyKey->'+familyKey);

List<List<String>> familyValues= familyMap.values();
System.debug('familyValues->'+familyValues);
List<list<String>> families = familyMap.values();
System.debug('families->'+families);
```
