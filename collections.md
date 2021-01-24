## Collections

### Iteration through List

This is an example of how to iterate through a list and add all the numbers together. 

```dart
var numbers = [1, 3, 5, 7, 9];
  var sum = 0;
  
  for(var number in numbers){
    sum = sum + number;
    
  }
  print(sum);
```

### Sets

Sets are very similar to lists because they both hold a collection of items. However, sets can only contain unique items and have specific functions.

The union() function combines the two sets together, but only repeats `Mali` once.

The intersection() function finds the country that both sets share which is `Mali`.

Lastly, the difference() function finds the countries in africanCountries that differ from asianCountries. 

```dart
var asianCountries = {'Japan', 'South Korea', 'Mali'};
  var africanCountries = {'Nigeria', 'South Africa', 'Mali'};
  print(africanCountries.union(asianCountries));
 print(africanCountries.intersection(asianCountries));
  print(africanCountries.difference(asianCountries));
```

The for in loop can be used to add all the values in a set together.

```dart
var sum = 0;
  for(var value in d){
    sum += value;
  }
  print(sum);
  
```

### Collection-if

The collection-if statement inside of a list runs an if statement and can add more items to the list. 

```dart
final colors2 = [
    'grey',
    'brown',
    if (addBlue)
      'blue',
    if (addRed)
      'red',]
```

### Spreads

The spread operator uses `...` to add elements of a list to the enclosing list/collection. The spread operator can be used inside of a list to add additional items.

The example below shows a collection-if statement being used in conjuction with the spread operator. The ratings list and the item `isPopular` is added to restaurant if the predicate returns true.

```dart
 const ratings = [4.0, 4.5, 3.5];
  final restaurant = {
    'name': 'Pizza Mario',
    'cuisine': 'Italian',
    if (ratings.length > 3) ...{
      'ratings': ratings,
      'isPopular': true,
    }
```

### Copying collections

If you copy a list like the example shown below, then it only copys the memory address. This address is invisible and is not the actual value of the list. When I try to change the first element of copy1, it also changes the first element of originalList

```dart
final originalList = [1,2,3];
final copy1 = originalList;
copy1[0] = 0;
```

To fix this problem, I used the spread operator which copies the actual values of the list. Thus, when I change the 3rd element of copy2, the originalList is not altered. 

```dart
final copy2 = [...originalList];
copy2[2] = 4;
```