A complete SeeSolve-style page that uses every tag in [[HTML Tags, Elements, Attributes]]. The table's "Common/ Used Lines" column points to these line numbers.

```html
  1. <!DOCTYPE html>
  2. <html lang="en"> **
  3. <head>
  4.   <meta charset="UTF-8">
  5.   <meta name="viewport" content="width=device-width, initial-scale=1.0">
  6.   <meta name="description" content="SeeSolve: a visual learning calculator">
  7.   <title>SeeSolve</title>
  8.   <link rel="stylesheet" href="styles/main.css">
  9.   <link rel="icon" href="icons/icon-192.png">
 10.   <style>
 11.     .answer { color: teal; }
 12.   </style>
 13. </head>
 14. <body>
 15.   <!-- Top of the page: logo and menu -->
 16.   <header>
 17.     <a href="index.html"><img src="icons/logo.png" alt="SeeSolve logo" width="40" height="40"></a>
 18.     <nav>
 19.       <ul>
 20.         <li><a href="#courses">Courses</a></li>
 21.         <li><a href="#solver">Solver</a></li>
 22.         <li><a href="https://github.com/YOURNAME/seesolve" target="_blank">GitHub</a></li>
 23.       </ul>
 24.     </nav>
 25.   </header>
 26. 
 27.   <main id="app">
 28.     <section id="courses">
 29.       <h1>Choose your course</h1>
 30.       <p>SeeSolve helps you <strong>see</strong> math and science, not just get <em>answers</em>.</p>
 31.       <h2>Mathematics</h2>
 32.       <ol>
 33.         <li>MTH1W: Mathematics, Grade 9</li>
 34.         <li>MCR3U: Functions, Grade 11</li>
 35.       </ol>
 36.       <hr>
 37.     </section>
 38. 
 39.     <section id="solver">
 40.       <h2>Solve an equation</h2>
 41.       <form id="solve-form">
 42.         <label for="problem">Problem</label>
 43.         <input type="text" id="problem" name="problem" placeholder="2x^2 - 3x - 2 = 0" required>
 44.         <label for="course">Course</label>
 45.         <select id="course" name="course">
 46.           <option value="mcr3u" selected>MCR3U</option>
 47.           <option value="sch3u">SCH3U</option>
 48.         </select>
 49.         <label for="a">a</label>
 50.         <input type="range" id="a" min="-5" max="5" step="0.5" value="1">
 51.         <output for="a" id="a-value">1</output>
 52.         <label><input type="checkbox" id="learn-mode" checked> Learn Mode</label>
 53.         <button type="submit">Solve</button>
 54.       </form>
 55.       <p>Answer: <span id="answer" class="answer">x = 2</span></p>
 56.       <p>Water is H<sub>2</sub>O and area is x<sup>2</sup>.<br>Try another problem.</p>
 57.       <canvas id="graph" width="600" height="400"></canvas>
 58.     </section>
 59. 
 60.     <article>
 61.       <h3>Step by step</h3>
 62.       <blockquote>Knowing why an answer works matters more than the answer.</blockquote>
 63.       <pre><code>x = (-b +/- sqrt(b^2 - 4ac)) / (2a)</code></pre>
 64.       <details>
 65.         <summary>Show hint</summary>
 66.         <p>Find the discriminant first.</p>
 67.       </details>
 68.     </article>
 69. 
 70.     <section>
 71.       <h2>Results table</h2>
 72.       <table>
 73.         <tr>
 74.           <th>Year</th>
 75.           <th>Amount ($)</th>
 76.         </tr>
 77.         <tr>
 78.           <td>0</td>
 79.           <td>1000.00</td>
 80.         </tr>
 81.       </table>
 82.     </section>
 83. 
 84.     <section>
 85.       <h2>Notes and feedback</h2>
 86.       <textarea id="notes" rows="4" cols="40" placeholder="I like... I wish... What if..."></textarea>
 87.       <div class="media">
 88.         <video src="media/intro.mp4" controls width="320"></video>
 89.         <iframe src="https://www.youtube.com/embed/VIDEO_ID" title="Intro video" width="320" height="180"></iframe>
 90.       </div>
 91.     </section>
 92.   </main>
 93. 
 94.   <aside>
 95.     <p>Tip: press Tab to move between inputs.</p>
 96.   </aside>
 97. 
 98.   <footer>
 99.     <p>&copy; 2026 SeeSolve, made for ICT SHSM at A.Y. Jackson S.S.</p>
100.   </footer>
101. 
102.   <script src="js/app.js" type="module"></script>
103. </body>
104. </html>
```
