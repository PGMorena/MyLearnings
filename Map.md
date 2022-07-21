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

```

# Store account vs contacts in map
```
Map<Id, List<Contact>> contactMap = new Map<Id, List<Contact>>();
List<Contact> conList = [Select Id, accountId from Contact];
for(Contact con: conList){
    if(!contactMap.containsKey(con.AccountId)){
           // List<Contact> newConList = new List<Contact>();
           // newConList.add(con);
            contactMap.put(con.AccountId, new List<Contact>{con});
    }else{
        //List<Contact> existingConList = contactMap.get(con.AccountId);
       // existingConList.add(con);
         contactMap.put(con.AccountId, contactMap.get(con.AccountId).add(con));
    }   
}
```
# Map with account id and no. of contacts
```
Map<Id, Integer> contactMap = new Map<Id, Integer>();
List<Contact> conList = [Select Id, accountId from Contact];
for(Contact con: conList){
    if(!contactMap.containsKey(con.AccountId)){
           // List<Contact> newConList = new List<Contact>();
           // newConList.add(con);
            contactMap.put(con.AccountId, 1);
    }else{
        //List<Contact> existingConList = contactMap.get(con.AccountId);
       // existingConList.add(con);
         contactMap.put(con.AccountId, contactMap.get(con.AccountId)+1);
    }   
}
```
# Count the number of occrurence of the integers
```
List<Integer> intList =new List<Integer>{1,2,3,1,1,2};
Map<Integer, Integer> intMap = new Map<Integer, Integer>();
 //count=0;
for(Integer i:intList){
if(!intMap.containsKey(i)){
       intMap.put(i,0);
     }
    Integer count=intMap.get(i)+1;
     intMap.put(i,count);
 }
```

#Another way
```
List<Integer> intList =new List<Integer>{1,2,3,1,1,2};
Map<Integer, Integer> intMap = new Map<Integer, Integer>();
 //count=0;
for(Integer i:intList){
if(!intMap.containsKey(i)){
       intMap.put(i,0);
     }
    if(intMap.containsKey(i)){
        Integer count = intMap.get(i)+1;
        intMap.put(i,count);
        System.debug('intMap'+intMap);
    }
 }
```
