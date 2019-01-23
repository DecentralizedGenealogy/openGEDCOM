# Sex (Gender)
The `sex` element is an ordered array. This is to accomodate those who have undergone hormonal or sugical changes, or identify themselves as something other than what physical sex classification was at birth. The first entry in the array is the current or default sex.

### Example 1
```
"sex": [
	{ "value": "female" }
]
```

### Example 2
This examples illustrates a person that was born as an [Intersex](https://en.wikipedia.org/wiki/Intersex), and later identified themselves (either by surgery or self-classification) as Male.
```
"sex": [
	{ "value": "male" },
	{ "value": "intersex" }
]
```