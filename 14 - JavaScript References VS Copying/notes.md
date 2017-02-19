# Console Tricks

If you don't know where the JS is getting triggers.

Inspect Element > Breakon > Attribute modifications
will add a debugger command

## Console.logging

Style the log message
`console.log('%cI am some great text', 'font-size: 50px');`

---

Message is highlighted yellow
`console.warn('OH NO!!')`

---

Error
`console.error('SHIT')`

---

Info
`console.info('Crocs eat 3-4 people per year')`

---

Assert will only run if something is wrong
`console.assert(1 === 2, 'That is wrong!')`

---

Clearing console (to mess with a dev)
`console.clear();`

---

View Dom Element
Actual elem: `console.log(p)`
Shows path: `console.dir(p)`

---

Grouping together
~~~
dogs.forEach(dog => {
    console.group(`${dog.name}`);
    console.log(`This is ${dog.name}`);
    console.log(`${dog.name} is ${dog.age}`);
    console.groupEnd(`${dog.name}``)
});
~~~

Can also use `console.groupCollapse` instead and it'll fold the logs

---

Counting
`console.count()` will iterate through and show the count of times it gets mentioned

---

Timing
See how long something takes
~~~
console.time('fetching data');
fetch('https://api.github.com/users/jennytran')
    .then(data => data.json())
    .then(data => {
        console.timeEnd('fetching data');
        console.log(data);
    })
~~~

---

For an array of objects in a table, i.e:
~~~
    const dogs = [
        {name: 'Snickers', age: 2},
        {name: 'Bob', age: 5}
    ];

    console.table(dogs);
~~~
