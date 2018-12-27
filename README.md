# christmas-presents
'Secret' santa between groups or families. Buy a present for someone random in another group. Or just match people/elements from different groups with each other.

People inside a certain group won't match with people in the same group.

# Add people
To clear all added people so far, call `clearPeople()`.
A person can be added by pushing a new `Person` object on the `people` array. Example:

```javascript
people.push(new Person('Person Name', 'Group Name'));
```

People get a unique ID and hence can have the same name. The person ID can be requested by calling `getId()` on the `Person` object. Group names are case sensitive, group `A` is a different group than `a`.

# Generate matches
There are three algorithms that can be called: `circleMatch()`, `randomMatch()` and `coupleMatch()`.

Just call the function and the matching algorithm will try to generate all matches between all groups. If succeeded, `True` is returned, `False` otherwise. Matches are stored in the `matches` array as `BuysFor` objects which contains two `People` objects.

# View matches
They are visualised with the function `printMatches(id)`. `id` is the id of a DOM UL-object where the matches will be displayed.

# Minimal demo
```javascript
clearPeople();
people.push(new Person('Person A', 'First group'));
people.push(new Person('Person B', 'Second group'));
if (randomMatch()) {
    printMatches(); // Append to body
}
```
