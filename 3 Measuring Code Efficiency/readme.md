# How to Measure Code Efficiency

আমরা যেকোন প্রবলেম এর অনেকভাবে সল্যুশন করতে পারি। এখন কোন অয়েতে সল্যুশন করলে এটা বেটার হবে তা কিভাবে measure করবো? যেমন আমরা নিচে একটা সমস্যা সমাধান করবো কয়েকভাবে

### suppose we want to write a function that calculates the sum of all numbers from 1 up to (and including) some number n.

```
With for loop

function sumUpTo (n){
    let total = 0;
    for(let i = 1; i <= n; i++>){
        total += i;
    }
    return total;
}

sumUpTo (10)
```

```
With for mathematical formula

function sumUpTo (n){
    return n * ( n + 1 ) / 2;
}

sumUpTo (10)
```

অর্থাৎ একই সমস্যার একাধিক সমাধান হতে পারে। এখানে আমরা বিভিন্ন অ্যালগরিদম ব্যাবহার করে একই সমস্যার সমাধান করেছি এবং একই রেজাল্ট পেয়েছি। এখন প্রশ্ন হচ্ছে কোনটা বেটার?

## What Does Better Mean?

- Faster in execution (Requires in less time)?
- Less Memory-Intensive (Requires in less memory)?
- More Readable?

### Measure Timings to Run The Code

```
function sumUpTo (n){
    let total = 0;
    for(let i = 1; i <= n; i++>){
        total += i;
    }
    return total;
}

const t1 = performance.now();
sumUpTo (10000000)
const t2 = performance.now();
console.log(`Time required: ${(t2 - t1) / 1000} seconds.`)
```

উপড়ের কোডটি রান করে আমরা দেখতে পারব আমাদের কোডটি রান করতে কত সময় লেগেছে। কিন্তু এভাবে তো আমরা আমাদের প্রত্যেক কোডের টাইম চেক করে করে কাজ করতে পারব না। আর এছাড়াও একেক মেশিনের কনফিগারেশনের উপর ভিত্তি করে একেক মেশিনে সেম কোডের জন্য আলাদা আলাদা সময় নিবে। তাই এটা উপজুক্ত কোন সমাধান নয় time mesaure করার জন্য।

Problem with Time

- Different machine will record different times
- The same machine will record different times
