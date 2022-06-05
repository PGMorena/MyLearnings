# Add in a list- way 1
```
List<String> lst = new List<String>{'apple','banana','orange'};
```
# Add in a list- way 2
```
List<String> lst = new List<String>();
lst.add('apple');
lst.add('banana');
lst.add('orange');
```
# Contains
```
boolean isGuavaExist = lst.contains('guava');
boolean isBananaExist = lst.contains('banana');
if(isGuavaExist == true){
   System.debug('Yes guava is there');
}
if(isGuavaExist == false){
   System.debug('No, Guava is not there');
}
if(isBananaExist == true){
   System.debug('Yes banana is there');
}
if(isBananaExist == false){
   System.debug('No, banana is not there');
}
```
```
if(lst.contains('guava') == true){
   System.debug('Yes guava is there');
}
if(lst.contains('guava') == false){
   System.debug('No, Guava is not there');
}
if(lst.contains('banana') == true){
   System.debug('Yes banana is there');
}
if(lst.contains('banana') == false){
   System.debug('No, banana is not there');
}
```
```
if(lst.contains('guava')){
   System.debug('Yes guava is there');
}
if(!lst.contains('guava')){
   System.debug('No, Guava is not there');
}
if(lst.contains('banana')){
   System.debug('Yes banana is there');
}
if(!lst.contains('banana')){
   System.debug('No, banana is not there');
}
```
```
String GuvaCheck = lst.contains('guava')? 'Yes guava is there': 'No, Guava is not there';
String BananaCheck = lst.contains('banana')? 'Yes banana is there': 'No, banana is not there';
System.debug(GuvaCheck);
System.debug(BananaCheck);
```
# Empty Check
```
List<String> lst = new List<String>();
/*lst.add('apple');
lst.add('banana');
lst.add('orange');*/
if(!lst.isEmpty()){
    String GuvaCheck = lst.contains('guava')? 'Yes guava is there': 'No, Guava is not there';
    String BananaCheck = lst.contains('banana')? 'Yes banana is there': 'No, banana is not there';
    System.debug(GuvaCheck);
    System.debug(BananaCheck);
}else{
    System.debug('There is nothing in the list');
}



```












