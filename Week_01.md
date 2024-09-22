## Guidance
Answer the following questions considering the learning outcomes for
- Week 01

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
>  using fetch and catch within a function
 
> [your evidence here]
> function getUser(username) {
        return fetch(`https://api.github.com/users/${username}`)
        .then(response => response.json());
      }
      getUser("rilez366")
      .then(user => console.log(user))
      .catch(error => console.log(error));

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> trying to get comfortable with all the css styling tools and the effects


> [your evidence here]
> /* Navbar styling */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  background-color: var(--background-light);
  position: sticky;
  width: 100%;
  top: 0;
  z-index: 1000;
}


## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
