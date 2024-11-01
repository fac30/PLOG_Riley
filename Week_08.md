## Guidance
Answer the following questions considering the learning outcomes for
- [Week 08](https://learn.foundersandcoders.com/course/syllabus/developer/week08-project04-test-deploy/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
>learning about render
> choosing render to deploy the backend on
> learning about permanant disks
> learning how to transfer data from SQLite to postgreSQL

> [your evidence here]
> export const createBuyer = async (username: string, email: string, hashedPassword: string): Promise<boolean> => {
    const query = 'INSERT INTO buyer (name, email, password) VALUES ($1, $2, $3) RETURNING id';  // Use $1, $2, $3 for parameterized queries

    return new Promise((resolve, reject) => {
        pool.query(query, [username, email, hashedPassword], (err, result) => {
            if (err) {
                console.error('Error creating user:', err);
                return reject(false);
            }
            if (result.rows.length > 0) {
                resolve(true);
            } else {
                console.error('Failed to create user: No rows returned');
                resolve(false);
            }
        });
    });
};

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> still learnimg the syntax behind postgreSQL
> difference between the 2 data types

> [your evidence here]

const addProduct = (product: Omit<Product, 'id'>): Promise<number> => {
  const { name, description, price } = product;
  return pool.query('INSERT INTO products (name, description, price) VALUES ($1, $2, $3) RETURNING id', [name, description, price]) // Use RETURNING to get the new ID
    .then(result => result.rows[0].id) 
    .catch(err => Promise.reject(err));
};

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
