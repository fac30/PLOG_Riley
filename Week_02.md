## Guidance
Answer the following questions considering the learning outcomes for
- [Week 02](https://learn.foundersandcoders.com/course/syllabus/developer/week02-project02-chatbot/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
> learning how to handle promises and whats the output of them
> learning the syntax of async functions 

> [your evidence here]

console.log('before');
new Promise(resolve => {
  setTimeout(resolve, 1000);
}).then(() => {
  console.log('first then is running');
}).then(() => {
  console.log('second then is running');
});

console.log('after');

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> get more comfortable with writing if statements 


> [your evidence here]
> // If no football opinions are provided, send a cheeky response back to the user
    if (!footballOpinions) {
      message.channel.send("You want me to give an opinion, but you don't even know about football? Wake up.");
      return; // Exit the function if no opinions are provided
    }

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
