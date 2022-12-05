---
permalink: /quiz
layout: page
search_exclude: false
title: Lists & Iteration Quiz
---

<body>

	<div id="quiz-container"></div>

	<script>
	
	const quiz_container = document.getElementById("quiz-container")
	
	// initialize dictionary
	const questions = {
		"What is Iteration defined as?":
			[1, 2, ["(a) Sequence of instructions", "(b) Repetition of a process", "(c) Boolean", "(d) List"]],
		"What is a List defined as?":
			[2, 1, ["(a) Collection of data in a sequence that is a iterable", "(b) Numbers", "(c) Selection between two paths based on solution", "(d) Groceries"]],
		"What does a “FOR LOOP” do? What is the variable, “i”, used for?":
			[3, 1, ["(a) FOR LOOP repeats a function for a set number of times; I is the number of times repeated", "(b) I is a parameter of the function, and for only performs an action if certain circumstances are met", "(c) The FOR LOOP is a function and I the absolute value of the function", "(d) The FOR LOOP controls the order functions are called on outside of the for loop; I is the number of functions it controls"]],
		"How can we add something to the end of a list?":
			[4, 3, ["(a) Use + sign", "(b) The word Add", "(c) Append", "(d) Extend"]],
		"What is Indexing / List Index defined as?":
			[5, 2, ["(a) Contents of List", "(b) The position of an element in a list, starting from 0", "(c) Alphabetical Ordered List", "(d) Measurement of List"]],
		"What does the POP command do?":
			[6, 4, ["(a) Removes a list", "(b) Adds a list", "(c) Adds to the end of List", "(d) Removes the last item from a list"]],
		"What is Base 0 Indexing?":
			[7, 4, ["(a) Binary", "(b) Mutation", "(c) Sequence demarcated with an Index starting from 1", "(d) Seguence demarcated with an Index starting from 0"]],
		"What does a WHILE loop do?":
			[8, 3, ["(a) Iterates over an iterable and for a set amount of time", "(b) Intuitively takes an iterable and manipulates it over a set period using pointers", "(c) Loop over a bound interval by comparing to a conditional", "(d) Crash bitcoin"]],
		"I want to iterate over a list until the user inputs 'quit'. What loop would I use?":
			[9, 2, ["(a) WHILE loops", "(b) FOR loops", "(c) Recursive Loops", "(d) Paradoxical Loops"]],
		"We have the list [['lizards', 'snakes', 'salamanders'], ['sharks', 'whales', 'fish'], ['lions', 'tigers', 'pumas']]. How many loops and of which type(s) would we need in order to iterate through every element in this list most efficiently?":
			[10, 1, ["(a) 2, both FOR loops", "1, a FOR loop", "2, a WHILE and a FOR loop", "2, both WHILE loops"]]
	}
	
	for (let question in questions) {
	
		// question wrapper
		let question_container = document.createElement("div")
		question_container.style.backgroundColor = "#f5f5f5"
		question_container.style.marginTop = "10px"
		question_container.style.marginBottom = "10px"
		question_container.style.padding = "15px"
		question_container.style.borderRadius = "18px"
	
		quiz_container.appendChild(question_container)
	
		// key in questions
		let prompt = document.createElement("h3")
		prompt.innerHTML = "#" + questions[question][0] + ") " + question
		prompt.style.marginBottom = "2px"
		prompt.style.marginTop = "2px"
	
		question_container.appendChild(prompt)
	
		// ul for answers
		let answers = document.createElement("ul")
		answers.style.listStyle = "none";
		answers.style.margin = "4px"
		answers.style.paddingLeft = "12px"
		answers.setAttribute("id", "answer-container-" + questions[question][0])
	
		question_container.appendChild(answers)
	
		let answer_num = 0
	
		for (let answer_choice in questions[question][2]) {
	
			answer_num += 1
	
			// creates answer choice 
			let answer_option = document.createElement("li")
			answer_option.style = "display:flex; align-items:center;"
			answer_option.style.cursor = "pointer";
			answer_option.style.borderRadius = "8px"
			answer_option.style.backgroundColor = "#e7e5e4"
			answer_option.style.marginTop = "8px"
			answer_option.setAttribute("id", answer_num)
	
	
			let answer_text = document.createElement("p")
			answer_text.style.marginLeft = "8px"
			answer_text.innerHTML = questions[question][2][answer_choice]
	
			answer_option.append(answer_text)
	
			// adds to DOM
			answers.appendChild(answer_option)
	
			// passes in question num & answer num
			answer_option.onclick = () => check_answer(questions[question][0], answer_option.id)
		}
	
	}
	
	function check_answer(question_num, answer_num) {
	
		// gets the answer element
		console.log("answer_num: " + answer_num)
		let answer_container = document.getElementById("answer-container-" + question_num)
		let selected_answer = answer_container.children[answer_num - 1]
		selected_answer.style.transition = "all .5s ease"
	
		console.log(Object.values(questions)[question_num - 1][1])
	
		// converts the dict to an array and accesses the answer by question_num
		if (Object.values(questions)[question_num - 1][1] == answer_num) {
			selected_answer.style.backgroundColor = "#bbf7d0";
			selected_answer.style.fontWeight = "bold";
		} else {
			selected_answer.style.textDecoration = "line-through";
			selected_answer.style.backgroundColor = "#fca5a5";
		}
	
	}
	
	</script>

</body>
