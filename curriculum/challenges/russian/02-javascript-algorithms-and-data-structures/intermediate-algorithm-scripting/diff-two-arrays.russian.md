---
id: a5de63ebea8dbee56860f4f2
title: Diff Two Arrays
isRequired: true
challengeType: 5
videoUrl: ''
localeTitle: Diff Два массива
---

## Description
<section id="description"> Сравните два массива и верните новый массив с любыми элементами, найденными только в одном из двух заданных массивов, но не обоих. Другими словами, верните симметричную разность двух массивов. Не забудьте использовать <a href="http://forum.freecodecamp.org/t/how-to-get-help-when-you-are-stuck/19514" target="_blank">Read-Search-Ask,</a> если вы застряли. Попробуйте подключить программу. Напишите свой собственный код. <strong>Заметка</strong> <br> Вы можете вернуть массив с его элементами в любом порядке. </section>

## Instructions
<section id="instructions">
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: '<code>diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5])</code> должен возвращать массив.'
    testString: 'assert(typeof diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]) === "object", "<code>diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5])</code> should return an array.");'
  - text: '<code>[&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;pink wool&quot;, &quot;dead shrub&quot;], [&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должен вернуть <code>[&quot;pink wool&quot;]</code> .'
    testString: 'assert.sameMembers(diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]), ["pink wool"], "<code>["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]</code> should return <code>["pink wool"]</code>.");'
  - text: '<code>[&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;pink wool&quot;, &quot;dead shrub&quot;], [&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должен возвращать массив с одним элементом.'
    testString: 'assert(diffArray(["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]).length === 1, "<code>["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]</code> should return an array with one item.");'
  - text: '<code>[&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;pink wool&quot;, &quot;dead shrub&quot;], [&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должен вернуться <code>[&quot;diorite&quot;, &quot;pink wool&quot;]</code> .'
    testString: 'assert.sameMembers(diffArray(["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]), ["diorite", "pink wool"], "<code>["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]</code> should return <code>["diorite", "pink wool"]</code>.");'
  - text: '<code>[&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;pink wool&quot;, &quot;dead shrub&quot;], [&quot;diorite&quot;, &quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должны возвращать массив с двумя элементами.'
    testString: 'assert(diffArray(["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]).length === 2, "<code>["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"]</code> should return an array with two items.");'
  - text: '<code>[&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;], [&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должны вернуться <code>[]</code> .'
    testString: 'assert.sameMembers(diffArray(["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"]), [], "<code>["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"]</code> should return <code>[]</code>.");'
  - text: '<code>[&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;], [&quot;andesite&quot;, &quot;grass&quot;, &quot;dirt&quot;, &quot;dead shrub&quot;]</code> должны возвращать пустой массив.'
    testString: 'assert(diffArray(["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"]).length === 0, "<code>["andesite", "grass", "dirt", "dead shrub"], ["andesite", "grass", "dirt", "dead shrub"]</code> should return an empty array.");'
  - text: '<code>[1, 2, 3, 5], [1, 2, 3, 4, 5]</code> должны вернуться <code>[4]</code> .'
    testString: 'assert.sameMembers(diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]), [4], "<code>[1, 2, 3, 5], [1, 2, 3, 4, 5]</code> should return <code>[4]</code>.");'
  - text: '<code>[1, 2, 3, 5], [1, 2, 3, 4, 5]</code> должны возвращать массив с одним элементом.'
    testString: 'assert(diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]).length  === 1, "<code>[1, 2, 3, 5], [1, 2, 3, 4, 5]</code> should return an array with one item.");'
  - text: '<code>[1, &quot;calf&quot;, 3, &quot;piglet&quot;], [1, &quot;calf&quot;, 3, 4]</code> должны возвращать <code>[&quot;piglet&quot;, 4]</code> .'
    testString: 'assert.sameMembers(diffArray([1, "calf", 3, "piglet"], [1, "calf", 3, 4]), ["piglet", 4], "<code>[1, "calf", 3, "piglet"], [1, "calf", 3, 4]</code> should return <code>["piglet", 4]</code>.");'
  - text: '<code>[1, &quot;calf&quot;, 3, &quot;piglet&quot;], [1, &quot;calf&quot;, 3, 4]</code> должны возвращать массив с двумя элементами.'
    testString: 'assert(diffArray([1, "calf", 3, "piglet"], [1, "calf", 3, 4]).length === 2, "<code>[1, "calf", 3, "piglet"], [1, "calf", 3, 4]</code> should return an array with two items.");'
  - text: '<code>[], [&quot;snuffleupagus&quot;, &quot;cookie monster&quot;, &quot;elmo&quot;]</code> должны возвращать <code>[&quot;snuffleupagus&quot;, &quot;cookie monster&quot;, &quot;elmo&quot;]</code> .'
    testString: 'assert.sameMembers(diffArray([], ["snuffleupagus", "cookie monster", "elmo"]), ["snuffleupagus", "cookie monster", "elmo"], "<code>[], ["snuffleupagus", "cookie monster", "elmo"]</code> should return <code>["snuffleupagus", "cookie monster", "elmo"]</code>.");'
  - text: '<code>[], [&quot;snuffleupagus&quot;, &quot;cookie monster&quot;, &quot;elmo&quot;]</code> должны возвращать массив с тремя элементами.'
    testString: 'assert(diffArray([], ["snuffleupagus", "cookie monster", "elmo"]).length === 3, "<code>[], ["snuffleupagus", "cookie monster", "elmo"]</code> should return an array with three items.");'
  - text: '<code>[1, &quot;calf&quot;, 3, &quot;piglet&quot;], [7, &quot;filly&quot;]</code> должны возвращать <code>[1, &quot;calf&quot;, 3, &quot;piglet&quot;, 7, &quot;filly&quot;]</code> .'
    testString: 'assert.sameMembers(diffArray([1, "calf", 3, "piglet"], [7, "filly"]), [1, "calf", 3, "piglet", 7, "filly"], "<code>[1, "calf", 3, "piglet"], [7, "filly"]</code> should return <code>[1, "calf", 3, "piglet", 7, "filly"]</code>.");'
  - text: '<code>[1, &quot;calf&quot;, 3, &quot;piglet&quot;], [7, &quot;filly&quot;]</code> должны возвращать массив с шестью элементами.'
    testString: 'assert(diffArray([1, "calf", 3, "piglet"], [7, "filly"]).length === 6, "<code>[1, "calf", 3, "piglet"], [7, "filly"]</code> should return an array with six items.");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function diffArray(arr1, arr2) {
  var newArr = [];
  // Same, same; but different.
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);

```

</div>



</section>

## Solution
<section id='solution'>

```js
// solution required
```
</section>
