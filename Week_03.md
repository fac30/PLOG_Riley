## Guidance
Answer the following questions considering the learning outcomes for
- [Week 03](https://learn.foundersandcoders.com/course/syllabus/developer/week03-project03-server/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
> imrpoving using node and getting more comfortable with it
> using express for the first time
> setting up the environment for a project for the first time
> getting api endpoints to connect to a database and provide data
> used jira for the first time in a project

> [your evidence here]
const OpenAI = require("openai");
const dotenv = require("dotenv");

dotenv.config();

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY, // Get the API key from the environment variable
});

async function getOpenAIReponse(country: string) {
  const completion = await openai.chat.completions.create({
    messages: [
      {
        role: "system",
        content: `Give me a fun fact about ${country}. Do not send any text other than the fact (e.g. sure!, can do! or ok!) Only refer to the country as 'this country'`,
      },
    ],
    model: "gpt-4o",
  });

  return completion.choices[0].message.content;
}

async function getDistance(country: string, country2: string) {
  const completion = await openai.chat.completions.create({
    messages: [
      {
        role: "system",
        content: `what is the distance between ${country} and ${country2} in km. Do not send any text other than the fact (e.g. sure!, can do! or ok!) Only refer to the country as 'this country'`,
      },
    ],
    model: "gpt-4o",
  });

  return completion.choices[0].message.content;
}

module.exports = {
  getOpenAIReponse,
  getDistance,
};

export {};


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
installing all of the dependencies
> getting better at using node
> using typescript syntax better
> 
> [your evidence here]
> my example would just be the project environment

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
