[![Build Status](https://travis-ci.org/justojs/justo-assert.svg)](https://travis-ci.org/justojs/justo-assert)

An assertion framework.

*Proudly made in Valencia, Spain, EU.*

## Install

`npm install justo-assert`

## Assertions

The assertion is similar to `Should.js` , but with `must`.

### must.be.equal(), must.be.eq(), must.not.be.equal() and must.not.be.eq()

Checks whether a value is equal to another:

```
x.must.be.equal(123);
x.must.be.eq(123);

x.must.not.be.equal(123);
x.must.not.be.eq(123);
```

### must.match() and must.not.match()

Checks whether a value matches a regular expression:

```
name.must.match(/^Anna/);
name.must.not.match(/^Anna/);
```

### must.be.same() and must.not.be.same()

Checks whether if a value is strictly another:

```
user1.must.be.same(user2);
user1.must.not.be.same(user2);
```

### must.be.between() and must.not.be.between()

Checks whether a value is whitin a range:

```
x.must.be.between(1, 10);
x.must.not.be.between(1, 10);
```

### must.be.lessThan(), must.be.lt(), must.not.be.lessThan(), must.not.be.lt()

Checks whether a value is less than another:

```
x.must.be.lessThan(y);
x.must.be.lt(y);

x.must.not.be.lessThan(y);
x.must.not.be.lt(y);
```

### must.be.greaterThan(), must.be.gt(), must.not.be.greaterThan() and must.not.be.gt()

Checks whether a value is not less than another:

```
x.must.be.greaterThan(y);
x.must.be.gt(y);

x.must.not.be.greaterThan(y);
x.must.not.be.gt(y);
```

### must.contain() and must.not.contain()

Checks whether a value contains another:

```
str.must.contain("a");
arr.must.contain("a");

str.must.not.contain("a");
arr.must.not.contain("a");
```

### must.be.in() and must.not.be.in()

Checks whether a value is in a string or array:

```
substr.must.be.in(str);
item.must.be.in(arr);

substr.must.not.be.in(str);
item.must.not.be.in(arr);
```

### must.have() and must.not.have()

Checks whether a value has a property set:

```
user.must.have("username")
user.must.have(["username", "password"]);
user.must.have({username: "usr", password: "pwd"});

user.must.not.have("username");
user.must.not.have(["username", "password"]);
user.must.not.have({username: "usr", password: "pwd"});
```

### must.haveAny()

Checks whether a value have, at least, a specified property:

```
user.must.haveAny(["username", "password"]);
user.must.haveAny({username: "usr", password: "pwd"});
```

### must.all.have() and must.not.all.have()

Checks whether all items of a list have a property or set of properties:

```
array.must.all.have(["username", "password"]);
array.must.all.have({state: "LOCKED"});

array.must.not.all.have(["posts"]);
array.must.not.all.have({posts: []});
```

### must.be.instanceOf() and must.not.be.instanceOf()

Checks whether the type of a value is the specified one:

```
x.must.be.instanceOf("Address");
x.must.be.instanceOf(Address);

x.must.not.be.instanceOf("Address");
x.must.not.be.instanceOf(Address);
```

### must.raise() must.not.raise()

Checks whether a function call throws an error:

```
fn.must.raise();
fn.must.raise(Error);
fn.must.raise(Error, ["arg1"]);
fn.must.raise(Error, ["arg1", "arg2"]);

fn.must.not.raise();
fn.must.not.raise(error);
fn.must.not.raise(error, ["arg1"]);
fn.must.not.raise(error, ["arg1", "arg2"]);
```
