## Guidance
Answer the following questions considering the learning outcomes for
- [Week 07](https://learn.foundersandcoders.com/course/syllabus/developer/week07-project04-authentication/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
 
> how to scratch test a function
> how to refactor your work to make it look neater
> how to use placeholders in a function so that the tests run to the point where it is retrieving from the database and then it throws a error so that you know that the function you wrote is working

> [your evidence here]
xport const createBuyer = async (username: string, email: string, hashedPassword: string): Promise<boolean> => {
    const query = 'INSERT INTO buyer (name, email, password) VALUES (?, ?, ?)';

    return new Promise((resolve, reject) => {
        db.run(query, [username, email, hashedPassword], function (err) {
            if (err) {
                console.error('Error creating user:', err);
                return reject(false);
            }
            if (this.lastID) {
                resolve(true);
            } else {
                console.error('Failed to create user: No lastID');
                resolve(false);
            }
        });
    });
};

- ypu can see the paramaters within the function that relates to the sql data tables
- the placeholders are then within the next line 

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]

> kept on using user instead of buyer which took up time as I thought there was a problem within my function
> writing and refactoring my sql table to ensure it is using a sessions id insteaf of a jwt token


> [your evidence here]
CREATE TABLE IF NOT EXISTS sessions (
    sid TEXT PRIMARY KEY,        -- Session ID
    sess TEXT,                   -- Session data (contains user ID and other data)
    expire INTEGER              -- Expiry timestamp
);

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
