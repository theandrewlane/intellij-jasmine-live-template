# Introduction

##### Note: This is not my original work, started with this [repository](https://github.com/gbritting/jasmine-jetbrains-live-templates).

### [Jasmine](http://jasmine.github.io/) ES6 Live Templates for use in [JetBrains](http://www.jetbrains.com) IDEs 

Jasmine is "a behavior-driven development (BDD) testing framework for JavaScript, Jasmine doesn’t rely on browsers, the Document Object Model (DOM) or other JavaScript libraries. Great for websites, node.js server-side coding, or any project running JavaScript, its clean syntax makes writing tests a breeze". ([Pivotal Labs](http://pivotallabs.com/tools/))

Live templates are abbreviations that are expanded into code fragments that you use to insert frequently-used code into your source. Live templates are a huge productivity boost, especially when constructing unit-tests where you find yourself repetitively creating suites and specs. Live Templates are available in all JetBrains IDEs including IntelliJ, PyCharm, WebStorm, PhpStorm and RubyMine.

### Why These Are Different

There are other Jasmine live templates out there but with these we have simplified the act of remembering the abbreviations used as the expansion characters for the code fragment. Generally, you start with *j* for **J**asmine, then use the humps in the [camel-case](http://en.wikipedia.org/wiki/CamelCase) Jasmine function or Jasmine matcher name.

For instance, *jbe*, **J**asmine **b**efore<b>E</b>ach, would expand the `beforeEach` live template giving you a Jasmine `beforeEach` setup function.

<pre><code>beforeEach(() => {

});</code></pre>

*jtb*, **J**asmine **t**o<b>B</b>e would expand the `toBe` matcher Live Template giving you a Jasmine `toBe` expect and matcher.

<pre><code>expect('actual').toBe('expected');</code></pre>

Every matcher Live Template also has a negative assertion (not) Live Template. For instance,

*jntb*, **J**asmine **n**ot **t**o<b>B</b>e would expand the negative `toBe` matcher Live Template giving you a Jasmine `not.toBe` expect and matcher.

<pre><code>expect('actual').not.toBe('expected');</code></pre>

# Installation:

To install this template, copy ```Jasmine.xml``` to the matching folder and restart IntelliJ

- Windows: [home directory]\.[product name][version number]\config\templates

	Example: `C:\Users\a500806\.IntelliJIdea2017.1\config\templates`
	
- MacOS: ~/Library/Preferences/[product name][version number]/templates

## Jasmine Suite, Spec, Setup and Teardown Live Templates
<small>(NOTE: these first 3 do not follow the camel-case abbreviation)</small>

`jdes` - **J**asmine Suite (<b>des</b>cribe)
    
    describe('suite title', () => {
 
    });

`jit` - **J**asmine Spec (<b>it</b>)

    it('spec title', () => {
    
    });
    
`jit*` - **J**asmine <i>Generator<i> Spec (<b>it</b>) (it with added generator functionality)

    it('spec title', co.wrap(function *() {
        yield //this line is executed first
        yield //this line is executed next
    }));
    
`jxit` - **J**asmine Pending Spec (<b>xit</b>)
 
     xit('should ', () => {
     
     }).pend('pending reason...');

`jits` - **J**asmine Spec (<b>it</b> and starts your spec with the word <b>s</b>hould)

    it('should ', () => {

    });

`jbe` - **J**asmine **b**efore<b>E</b>ach (setup)

    beforeEach(() => {

    });
    
`jba` - **J**asmine **b**efore<b>A</b>ll (setup)

    beforeAll(() => {

    });

`jae` - **J**asmine **a**fter<b>E</b>ach (teardown)

    afterEach(() => {

    });
    
 `jaa` - **J**asmine **a**fter<b>A</b>ll (teardown)
 
     afterAll(() => {
 
     });

## Jasmine Matchers
`jtb` - **J**asmine **t**o<b>B</b>e `expect(x).toBe(y));`

`jtbd` - **t**o<b>B</b>e<b>D</b>efined `expect(x).toBeDefined());`

`jtbf` - **t**o<b>B</b>e<b>F</b>alsy `expect(x).toBeFalsy());`

`jtbgt` - **t**o<b>B</b>e<b>G</b>reater<b>T</b>han `expect(x).toBeGreaterThan(y));`

`jtblt` - **t**o<b>B</b>e<b>L</b>ess<b>T</b>han `expect(x).toBeLessThan(y));`

`jtbn` - **t**o<b>B</b>e<b>N</b>ull `expect(x).toBeNull());`

`jtbt` - **t**o<b>B</b>e<b>T</b>ruthy `expect(x).toBeTruthy());`

`jtbu` - **t**o<b>B</b>e<b>U</b>ndefined `expect(actual).toBeUndefined();`

`jtc` - **t**o<b>C</b>ontain `expect(x).toContain(y));`

`jte` - **t**o<b>E</b>qual `expect(x).toEqual(y));`

`jtm` - **t**o<b>M</b>atch `expect(x).toMatch(y));`

`jtt` - **t**o<b>T</b>hrow `expect(fn).toThrow(e));`

## Negated Matchers
`jntb` - **n**ot **t**o<b>B</b>e `expect(x).not.toBe(y));`

`jntbd` - **n**ot  **t**o<b>B</b>e<b>D</b>efined `expect(x).not.toBeDefined());`

`jntbf` - **n**ot  **t**o<b>B</b>e<b>F</b>alsy `expect(x).not.toBeFalsy());`

`jntbgt` - **n**ot  **t**o<b>B</b>e<b>G</b>reater<b>T</b>han `expect(x).not.toBeGreaterThan(y));`

`jntblt` - **n**ot  **t**o<b>B</b>e<b>L</b>ess<b>T</b>han `expect(x).not.toBeLessThan(y));`

`jntbn` - **n**ot  **t**o<b>B</b>e<b>N</b>ull `expect(x).not.toBeNull());`

`jntbt` - **n**ot  **t**o<b>B</b>e<b>T</b>ruthy `expect(x).not.toBeTruthy());`

`jntbu` - **n**ot  **t**o<b>B</b>e<b>U</b>ndefined `expect(actual).not.toBeUndefined();`

`jntc` - **n**ot  **t**o<b>C</b>ontain `expect(x).not.toContain(y));`

`jnte` - **n**ot  **t**o<b>E</b>qual `expect(x).not.toEqual(y));`

`jntm` - **n**ot  **t**o<b>M</b>atch `expect(x).not.toMatch(y));`

`jntt` - **n**ot  **t**o<b>T</b>hrow `expect(fn).not.toThrow(e));`
