## Guidance
Answer the following questions considering the learning outcomes for
- [Week 04](https://learn.foundersandcoders.com/course/syllabus/developer/week04-project03-frontend/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
Learning how to use jira for the first time
> learning how to be pm for first time and assign the correct tickets
> learning how to work with react for the first time
> learning how to work with tailwind for the first time

> [your evidence here]
> // ScoreDisplay component takes two props: displayType and score
const ScoreDisplay = ({ displayType, score }) => {
  return (
    // Display the score in an h2 element with styling classes for font size and margin
    <h2 className="text-xl mb-2">
      {/* Conditional rendering: If displayType is "highScore", display "High", otherwise display "User" */}
      {displayType === "highScore" ? "High" : "User"} score: {score}
    </h2>
  );
};

export default ScoreDisplay; // Export the component for use in other parts of the app


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> struggling with tailwind and how to style
> trying to keep up with all the tickets and assign them to correct people and designate to correct area
> React components and how props work
> [your evidence here]
> const CountryFact = ({ fact }: CountryFactProps) => {
  return <h2 className="m-auto w-3/6 text-center">{fact}</h2>;
};

--- <div className=" h-[210px] w-[200px] text-center float-right mr-[21px] relative bottom-[400px]">

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
