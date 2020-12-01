# Random:

`$sample`
-> Randomly selects the specified number of documents from its input.

### with Mongoose:

Return 1 random user
```js
const user = await User.aggregate([{ $sample: { size: 1 } }]);
```