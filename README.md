# christmas-presents
'Secret' santa between groups or families. Buy a present for someone random in another group. Or just match people/elements from different groups with each other.

People inside a certain group won't match with people in the same group.

# Add people
To clear all added people so far, call `clearPeople()`.
A person can be added by pushing a new Person object on the `people` array. Example:
```javascript
people.push(new Person('Person Name', 'Group Name'));
```
# Generate matches
There are three algorithms that can be called: `circleMatch()`, `randomMatch()` and `coupleMatch()`.

Just call the function and the will be one try to generate all matches. If succeeded, `True` is returned, `False` otherwise.

# View matches
Matches are stoder in the `matches` array. It contains `BuysFor` objects which contains two `People` objects.
They are visualised with the function `printMatches(id)`. `id` is the id of a DOM UL-object where the matches will be written.
