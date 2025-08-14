<h1>Hello, Traveler</h1>
<a href="https://discordapp.com/users/394185816370315276" target="_blank"><img alt="Contact Me" src="https://img.shields.io/badge/Contact_Me-gray?style=flat&logo=Discord&logoColor=white&logoSize=auto&labelColor=cornflowerblue"></a>
<a href="https://linktr.ee/swingthevine" target="_blank"><img alt="Linktree" src="https://img.shields.io/badge/Linktree-gray?style=flat&logo=Linktree"></a>
<br>
I am a programmer called SwingTheVine. I've programmed numerous projects since 2012. Some of the projects I am working on right now are:
<ul>
  <li>A userscript for wplace.live called <a href="https://github.com/SwingTheVine/Wplace-BlueMarble" target="_blank" rel="noopener noreferrer">Blue Marble</a></li>
  <li>A Minecraft mod called <a href="https://github.com/SwingTheVine/QSAND-Minecraft" target="_blank" rel="noopener noreferrer">QuickSand And Numerous Dungeons</a></li>
  <li>The website for <a href="https://github.com/SwingTheVine/TheBlueCorner-Website" target="_blank" rel="noopener noreferrer">The Blue Corner</a> community</li>
</ul>
If you like what I make, consider donating!
<br>
<a href='https://ko-fi.com/P5P1TW1PB' target='_blank' rel="noopener noreferrer"><img height='48' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
<br>
<a href="" target="_blank" rel="noopener noreferrer"><img src="https://github-readme-stats.vercel.app/api?username=swingthevine&show_icons=true&theme=transparent"/></a>
<h2>Join My Discord!</h2>
<a href="https://discord.gg/tpeBPy46hf" rel="noopener noreferrer"><img alt="Discord Banner" src="https://discord.com/api/guilds/796124137042608188/widget.png?style=banner4"></a>
<br>
<h2>Code Style</h2>
My coding style is similar to Kernighan & Ritchie (K&R), with a few changes to make the code more readable. In the examples, a "logic block" is a bunch of lines of code/comments that have a single, unified purpose. Comments that explain the code style (but are not a part of the style itself) are "legal comments" which use <code>/*! foobar */</code> instead of <code>/* foobar */</code>.
<details>
  <summary>
    JavaScript coding style example <sup>(click to expand)</sup>
  </summary>
  
  ```js
  /** This is a summary of the file's purpose as a top-of-file JSDoc comment.
  * This is an optional, detailed explanation.
  * The first line of the comment should be 1 sentence.
  * If more sentences are needed, they are put after the first line.
  * @since 1.2.3
  * @author SwingTheVine
  */

  /*! Import lines go here, usually in 1 logic block */
  import fs from 'fs';
  import { foo, bar } from './foobar.js';
  import { foo } from './foobar.js'; /*! There is ALWAYS a whitespace around the braces for imports. */

  /*! Import lines can optionally be grouped into logic blocks, based on type.
   * For example, all default imports could be grouped together, or all "require" imports could be in a different logic block from the "import"s.
   * If multiple logic blocks are used. There must ALWAYS be a comment before the logic block that explains the common logic of why all of the imports are in this specific logic block.
   * If there are multiple import logic blocks, there must ALWAYS be 1 blank line between them.
   */
  // CommonJS "imports" which require "require" in order to be imported
  import { createRequire } from 'module';
  const require = createRequire(import.meta.url);
  const terser = require('terser');
  const foo = require('foo');

  /*! There should ALWAYS be 1 blank line between the last import logic block, and the class definition logic block. */
  
  /** A 1 sentence description of what the class does.
   * An optional multi-line detailed description of what the class does.
   * @class Foo
   * @since 1.2.3
   * @example
   * // An example of how to use the Foo class
   */
  export default class Foo {
    /* An optional multi-line comment to further explain things about the Foo class.
     * This is rarely used, but comes in handy when you want to explain how the inside of the class works, but you don't want to flood the class JSDoc comment with details, since the JSDoc should only contain information about how to *use* the class and what the class *does*, not how the class *works*.
     * This multi-line comment should ALWAYS be right under the class definition.
     */

    /*! There should ALWAYS be 1 blank line after the logic block that defines the class. */

    /** This line should declare if this is the main constructor, or an overload.
     * An optional description of why this constructor should be used.
     * @param {*} foo - What foo is.
     * @param {*} bar - What bar is.
     * @since 1.2.3
     * @see {@link Foo}
     */
    constructor(foo, bar) { /*! Opening braces are ALWAYS on the same line as declaration */
      /*! There should NEVER be a whitespace before the first variable, and after the last variable. */

      /*! The blank line after the declaration is optional for constructors */
      this.foo = foo; // The description of foo should go here only if there is no JSDoc...
      this.bar = bar + 5; // ...but if the passed in variable is modified, a comment should be added to explain why.
      this.hatMan = 'a'; /*! Constants are ALWAYS camelCase */
      this.color = foo.RED_APPLE; /*! Enum variables are ALWAYS SCREAMING_SNAKE_CASE */
      /*! There is NEVER a blank line after the end of the last logic block in a statement */
    }
    /*! Closing braces are ALWAYS on their own line if the statement contains more than 1 line of code.
     * The closing brace is aligned with start of the statement.
     * However, if there are multiple closing braces, they can optionally be stacked onto the same line.
     */

    /** A 1 sentence description of what the function does.
     * An optional multi-line detailed description of what the function does.
     * @param {*} foo - What foo is.
     * @param {*} [bar=''] - What bar is.
     */
    function bar(foo, bar='') { /*! There should NEVER be a whitespace between the function name and the passed in variables.
     * There should NEVER be a whitespace before the first variable passed in when the variables are all on the same line as the function declaration.
     * There should NEVER be a whitespace after the last variable passed in when the variables are all on the same line as the function declaration.
     */
      /* An optional multi-line comment to further explain things about the bar function.
      * This is rarely used, but comes in handy when you want to explain how the inside of the function works, but you don't want to flood the function JSDoc comment with details, since the JSDoc should only contain information about how to *use* the function and what the function *does*, not how the function *works*.
      * This multi-line comment should ALWAYS be right under the function definition.
      */

      /*! There should ALWAYS be 1 blank line after the logic block that defines the function. */

      // Logic blocks with short comments use single-line comments.
      // Even if multiple single-line comments are needed.
      foo = `${foo} ${bar} + 5 foos`; /*! Template literals are prefered over strings when concatenating. */
      const barfoo = foo + 'apple'; /*! There should ALWAYS be a whitespace before and after math operators that do not use parentheses. */
      const flap = String.toLowerCase(foo + '.'); /*! There should NEVER be whitespaces after the opening parentheses, and before the closing parentheses (assuming the parentheses are on the same line). */

      /*! There should ALWAYS be 1 blank line between logic blocks. */

      // IF bar exists, AND the length of bar is greater than 0...
      if (!!bar && bar.length > 0) {

        // ...then prepend bar to foo
        const goo = `${bar}${foo}`;
        foo = goo;
      }

      // IF foo exists, then set bar to foo
      if (!!foo) {
        bar = foo; /*! When the entire conditional statement is 1 logic block, which includes all code within the conditional statement, and the conditional statement itself, there is NEVER a blank line after the statement declaration. */
      }

      /*! The comment line immediately above conditional statments SHOULD be spoken form of the conditional statement.
       * In addition, the comment ALWAYS uses all captital letters for logical operators and conditional statements.
       * E.g., "IF", "ELSE IF", "AND", "WHILE", "XOR", "NOT", "NOR", "greater than", "integer", "one", "bitwise OR", "then", "try", "exists"
       * In addition, the comment ALWAYS ends with an eclipse.
       * The eclipse is continued on the start of the next comment inside the conditional statment, and finishes the "thought" about what the conditional statement does.
       * If multiple comments are needed, then they MAY all start and end with eclipses to show a"continual thought process" that requires you to read multiple lines of comments, which arescattered apart.
       * However, if the conditional statement is 1 logic block, which includes all code within the conditional statement, and the conditional statement itself, then no eclipse is added, and the purpose of the logic statement is combined with the comment line that contains the spoken form of the conditional statement.
       * If nested logic is used within the conditional statement, it is written as follows...
       */

      // IF foobar exists...
      // ...AND foo exists...
      //    ...OR bar exists, AND goo exists...
      if (!!foobar && (!!foo || (!!bar && !!goo))) {

        // ...then set foobar to bar
        let goo = foo * bar; // Describe why foo * bar is used
        goo += 5; // Describe why 5 is being added here
        foobar = goo;
      }

      // Sum 1 + 1, then try to set a & b to the result
      const sum = ((a, b) => (a + b)); /*! Parentheses MIGHT be used around arrow functions and IIFEs. */
      try {
        const a, b = sum(1, 1);
      } catch (exception) { /*! It is perfered that the caught error variable be named "exception" */
        throw new Exception('lol get pwned');
      }
    } /*! There is ALWAYS no blank line after the last logic block, and the ending brace. */

    /** A 1 sentence description of what the function does.
     * An optional multi-line detailed description of what the function does.
     * @param {Object} [object] - NEVER describe the optional object here unless there are multiple objects being passed in.
     * @param {Array<string>} [object.never] - What never is.
     * @param {string} [object.gonna] - What gonna is.
     * @param {Boolean} [object.give] - What give is.
     * @param {Number} [object.number] - What you is.
     * @param {Number} [object.up] - What's up.
     * @since 1.2.3
     * @author SwingTheVine
     * @example
     * // One example
     * @example
     * // One example
     * @example
     * // One example
     */
    function #foo({
      never: [''], // A comment should describe each default value of these, ONLY if not described in @param
      gonna: '', // Going to hold "foobar" in gonna, or default to empty string if nothing is passed in.
      give: true,
      you: 1,
      up: 0.5, /*! Trailing comment is ALWAYS used on the last variable in objects UNLESS it causes lint warnings or errors. */
    } = {}) {

      never = ['foo', 'bar']; /*! Trailing comment is NEVER used on the last index of an array UNLESS it causes lint warnings or errors. */

      /*! Variables are named in the order of their most common denominator of what property they share. */
      const fooApple = undefined;
      const fooBar = undefined;
      const fooBarCarrot = undefined;
      const fooBarCarrotColor = 'orange';
      const fooHit = 'hurts others';
      const fooHitByBarFight = 'hurts me';
      const fooHitByTruck = 'hurts me more';

      /*! And the variable declarations can be in logic blocks */
      const bars = undefined;
      const barsLocations = undefined;
      const barsApple = undefined

      const barDrink = undefined;

      return true;
    }

    // Assume there is a JSDoc comment here
    function call() {

      #foo({
        you: false,
      });
    }
  }
  ```
</details>