## Guidance
Answer the following questions considering the learning outcomes for
- [Week 05](https://learn.foundersandcoders.com/course/syllabus/developer/week05-project03-test-deploy/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
> looking in to testing with cypress
> looking in to ci/cd pipelines


> [your evidence here]
> it("the features on the homepage are correct", () => {
      cy.get("dt").eq(0).contains("4 Courses")
      cy.get("dt").eq(1).contains("25+ Lessons")
      cy.get("dt").eq(2).contains("Free and Open Source")
    })
  })

CI/CD pipelines 
Step 1- create a workflow
Step 2- ensure that everything is being pushed to the master branch
Step 3- the event triggers a job that runs on a linux container that runs on the cloud 
Step 4- then we tell the container what to do and gives it various steps to abide by 
Step 5- it checks through the code on the github repo
Step 6- it ensures that node is fully set up and is running smoothly
Step 7- it will run the tests first
Step 8 - it will then run the build
Step 9 - it will then deploy
Step 10- anytime everything is pushed it goes to the master brunch and the pipeline will follow this whole workflow


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> making sure we are using the cprrect local host
> learning about differanrt ci/cd pipelines and how some are set up manually
> learning about all of the testing and using the correct methods
> using the correct typescript
> [your evidence here]
>  it("Course: Testing Foundations", () => {
      cy.getByData("course-1").find("a").contains("Get started").click()
      cy.location("pathname").should("equal", "/testing-foundations")
    })

    it("Course: Cypress Fundamentals", () => {
      cy.getByData("course-2").find("a").contains("Get started").click()
      cy.location("pathname").should("equal", "/cypress-fundamentals")
    })
  })
})

## Feedback (For CF's)
> [**Course Facilitator name**]

Alexander

> [*What went well*]

Basic understanding of Cypress testing with some practical examples. Good high-level overview of CI/CD pipeline steps.

> [*Even better if*]

Show actual CI/CD workflow file instead of just listing steps. Your Cypress tests are basic - demonstrate more complex test scenarios with user interactions or data validation.
