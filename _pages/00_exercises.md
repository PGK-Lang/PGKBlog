---
permalink: /exercises
layout: page
search_exclude: false
title: Lists & Iteration Exercises
---

# How to use
 - Below are code editors that you can use to develop answers to our exercises. We don't have the resources for a cloud-based compiler so you will have to copy what you write into your blog to interperet the output!

# Exercise #1
 - Task
   - Reverse a list utilizing features of lists and iteration 
     - Hint: Use two parameters with the range function
 - Expected Output
   - ```
     5
     4
     3
     2
     1
     ```

<html>
<div class="editor-container">Hello
  <div id="editor">list = [1, 2, 3, 4, 5] # Print this list in reverse order
  </div>
</div>

<h1>Exercise #2</h1>


<ul>
  <li>Task</li>
    <ul>
      <li>Similar to insertion sort, this algorithm takes an unsorted array and returns a sorted array</li>
      <li>Unlike insertion sort where you iterate through the each element and move the smaller elements to the front, this algorithm starts at the beginning and swaps the position of every element in the array</li>
    </ul>
  <li>Expected Output</li>
    <ul>
      <li>The sorted array from 1-10</li>
    </ul>
</ul>
  
<div class="editor-container2">
  <div id="editor2">list = [9, 8, 4, 3, 5, 2, 6, 7, 1, 0] # Sort this array using bubble sort
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/ace/1.13.1/ace.js"
  integrity="sha512-IQmiIneKUJhTJElpHOlsrb3jpF7r54AzhCTi7BTDLiBVg0f7mrEqWVCmOeoqKv5hDdyf3rbbxBUgYf4u3O/QcQ=="
  crossorigin="anonymous" referrerpolicy="no-referrer"></script>
<script>
  var editor = ace.edit("editor");
  editor.setTheme("ace/theme/clouds");
  editor.session.setMode("ace/mode/python");

  var editor2 = ace.edit("editor2");
  editor2.setTheme("ace/theme/clouds");
  editor2.session.setMode("ace/mode/python");
</script>

<style>
  .editor-container {
    width: 900px;
    height: 540px;
    margin: 24px auto;
    position: relative;
  }

  #editor {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    height: 100%;
    width: 100%;
    font-size: 20px;
  }

  .editor-container2 {
    width: 900px;
    height: 540px;
    margin: 24px auto;
    position: relative;
  }

  #editor2 {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    height: 100%;
    width: 100%;
    font-size: 20px;
  }
</style>

</html>
