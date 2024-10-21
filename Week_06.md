## Guidance
Answer the following questions considering the learning outcomes for
- [Week 06](https://learn.foundersandcoders.com/course/syllabus/developer/week06-project04-databases/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
> learning about SQL
> learning about relationships within SQL
> learning about how routes work
> turning schema data in to sql data


> [your evidence here]

>INSERT OR REPLACE INTO products VALUES
  (1, 'Football Boots', 'https://example.com/football-boots.jpg', 'Professional-grade football boots', 'High-performance footwear designed for serious football players', 100, 1, 1, NULL, 1),
  (2, 'Goalkeeper Gloves', 'https://example.com/goalkeeper-gloves.jpg', 'Pro-level goalkeeper gloves', 'High-grip gloves designed for maximum ball control and hand protection', 100, 1, 1, NULL, 1),
  (3, 'Premium Acrylic Paint Set', 'https://example.com/acrylic-paint-set.jpg', 'Vibrant colors for artistic expression', 'High-quality acrylic paint set with 24 rich, long-lasting colors perfect for canvas, wood, and more', 100, 1, 2, NULL, 2),
  (4, 'Artist Paint Brush Set', 'https://example.com/paint-brush-set.jpg', 'Professional-quality brushes for every technique', 'Versatile 15-piece brush set including flat, round, and detail brushes for acrylic, oil, and watercolor painting', 100, 1, 2, NULL, 2),
  (5, 'Flower Seeds Mix', 'https://example.com/flower-seeds.jpg', 'Colorful variety for your garden', 'A diverse mix of annual and perennial flower seeds to create a vibrant and beautiful garden', 100, 1, 3, NULL, 3),
  (6, 'Pruning Shears', 'https://example.com/pruning-shears.jpg', 'Sharp and precise garden tool', 'High-quality stainless steel pruning shears for effortless trimming of plants and small branches', 100, 1, 3, NULL, 3);

import db from '../config/db';

interface Product {
  id?: number;
  name: string;
  description: string;
  price: number;
}

// Function to get all products
const getAllProducts = (): Promise<Product[]> => {
  return new Promise((resolve, reject) => {
    const query = 'SELECT * FROM products';
    
    db.all(query, [], (err: Error | null, rows: Product[]) => {
      if (err) {
        reject(err);
      } else {
        resolve(rows);
      }
    });
  });
}; 

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> struggled with my terminal a bit this week and was getting a couple errors
> realsing certain syntax problems
> struggled with sql key concepts at first
 
> [your evidence here]

>CREATE TABLE IF NOT EXISTS "order" (
    id INTEGER PRIMARY KEY,
    items INTEGER,
    buyer INTEGER,
    CONSTRAINT fk_order_buyer FOREIGN KEY (buyer) REFERENCES buyer(id)
);

CREATE TABLE IF NOT EXISTS order_item (
    id INTEGER PRIMARY KEY,
    product INTEGER,
    "transaction" INTEGER,
    CONSTRAINT fk_order_item_product FOREIGN KEY (product) REFERENCES product(id),
    CONSTRAINT fk_order_item_order FOREIGN KEY ("transaction") REFERENCES "order"(id)
); 

## Feedback (For CF's)
> [**Course Facilitator name**]
>
> Alexander
> 
[*What went well*]  
It is great that you added code snippets, but you also need to explain what you mean with those. 
