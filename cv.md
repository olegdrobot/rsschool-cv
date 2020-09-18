## Oleg Drobot
***
### Contact Info
- **Email:** drobotoo@gmail.com
- **WhatsApp:** +7 (989) 721-70-16 

### Summary
***
I want to become a programmer and work in IT. I liked make a progamms code when I studyed at school and university. Although I chose another professional way in the deep of my soul I still want to be a programmer. It's interesting for me. I like learning. I tried to learn Java in the last year, now I'm learning JS, PHP, HTML. 

### Skills
***
* HTML/CSS;
* Git;
* Markdown;
* JavaScript;
* PHP.

### Code examples
***
~~~
<!DOCTYPE html>
<html lang="ru">
<head>
	<meta charset="UTF-8">
	<title>Students</title>
	<style>
    	body {
     		  text-align: left;
          height: 2000px;
          font-size: 18px;
        	background: #fcf3b5;
	    }

		  select
		  label
		  button {
  			width: 15%;
  			height: 5%;
  			padding-left: 5px;
  			font-size: 20px;
  			border-radius: 5px;
  		}

		  .line {
			  background: #000;
		  }

	</style>
</head>
<body >
    
    <label for="group">Group:</label>
    	<select class="allgroups">
      		<option value="1">Group 1</option>
      		<option value="2">Group 2</option>
      		<option value="3">Group 3</option>
    	</select>
    <label for="lesson">Lesson:</label>
    	<select class="all_lessons">
      		<option value="1">Lesson 1</option>
      		<option value="2">Lesson 2</option>
      		<option value="3">Lesson 3</option>
    	</select>
    <button type="button" class="btn">Select</button>
	<hr class="line">
  <div class="student"></div>
  <div class="save_student"></div>

<script>

  class JournalObj {
    gr ="";
    lesson ="";
    topic ="";

    students=[[]];
  }

  let journal=[];
   
	let btn = document.querySelector(".btn");
	console.log(btn);
	let allGroups = document.querySelector(".allgroups");
	console.log( allGroups);
	let allLessons = document.querySelector(".all_lessons");
	console.log(allLessons);

		let groups = [
  			{
    			group: 1,
    			students: ["student 1", "student 2", "student 3" ]
  			},
  			{
    			group: 2,
    			students: ["student а", "student б", "student в" ]
  			},
  			{
    			group: 3,
    			students: ["student a", "student b", "student c" ]
  			}
			];

	btn.addEventListener("click", function() {
    let f=false;
  	let out = document.querySelector(".student");
  	 out.innerHTML = "";
    let t = document.querySelector(".save_student");
     t.innerHTML = "";

 	if (journal.length!=0){
    for(i=0; i<journal.length;i++){
        if ((journal[i].gr==allGroups.value)&&(journal[i].lesson==allLessons.value)) {
          showJournal(journal[i]);
          f=true;
          console.log(f);
          break;
        }
    }
  }
   
  if (f){ return;}
  console.log(f+'  !!!!');
    
    let lessonName = document.createElement("div");
  	
 	  lessonName.className = "lesson_name";
    	lessonName.innerHTML = '<label for="topic">Topic: </label><input type="text" id="topic">';
  	  out.append(lessonName);
  	  console.log(lessonName);
  	
    	for (var item of groups) {
      	if (item.group == allGroups.value) {
     	  	 for (let i = 0; i <item.students.length; i++) {
          let studentsCheck = document.createElement("div");
          studentsCheck.innerHTML = '<label>' + item.students[i] + '<input type="checkbox" id="ch" class="check"></label>';
          out.append(studentsCheck);
        }
      }
    
      }
  
	  let saveButton = document.createElement("button");
  	  	saveButton.innerHTML = "Save";
  		  saveButton.style.height = "25px";
  		  saveButton.style.width = "80px";
        saveButton.addEventListener('click',saveJournal);
 	   out.append(saveButton); 
});

  function saveJournal(){
 
    let sts=document.querySelectorAll("label");
    console.log(sts);
    let out = document.querySelector(".save_student");
    
      out.innerHTML+='Group: '+allGroups.value+'  ';
      out.innerHTML+='Lesson: '+allLessons.value+'<br>';
      out.innerHTML+='Topic: '+document.getElementById('topic').value+'<br>';
    let jr = new JournalObj();
       jr.gr = allGroups.value;
       jr.lesson = allLessons.value;
       jr.topic = document.getElementById('topic').value;

    for (i=3; i<sts.length; i++){
      console.log(sts[i].lastChild.checked);
     if (sts[i].lastChild.checked){out.innerHTML+=sts[i].textContent+'  present'+'<br>';}
     else {out.innerHTML+=sts[i].textContent+'<br>';}
     jr.students[i-3]=[2];
     jr.students[i-3][0] = sts[i].textContent;
     jr.students[i-3][1] = sts[i].lastChild.checked;
    }
    journal.push(jr);
    console.log(journal);
    let t = document.querySelector(".student");
     t.innerHTML = "";
  }

  function showJournal(jour){
      
      let out = document.querySelector(".save_student");
      out.innerHTML+='Group: '+jour.gr+'  ';
      out.innerHTML+='Lesson: '+jour.lesson+'<br>';
      out.innerHTML+='Topic: '+jour.topic+'<br>';

      for(i=0; i<jour.students.length; i++){
        if (jour.students[i][1]){out.innerHTML+=jour.students[i][0]+'  present'+'<br>';}
        else {out.innerHTML+=jour.students[i][0]+'<br>'};
      }

  }
	</script>

</body>
</html>
~~~

### Experience

***

### Education
***
[Donetsk National Technical University](http://donntu.org/)/[Донецкий Национальный Технический Университет](http://donntu.org/)

### English
***
My English level is A2.
