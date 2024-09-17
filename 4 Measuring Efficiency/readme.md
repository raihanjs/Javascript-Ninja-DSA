# How to measure efficiency-counting operatior

আগে আমরা দেখলাম আসলে টাইম দিয়ে আমরা কোন সমাধানে আস্তে পারলাম না। আমরা আরেকটা কাজ করতে পারি। আমরা অপারেশন কাউন্ট করতে পারি। অপারেশন বলতে আমাদের কোডে কয়টা অপারেশন হচ্ছে।

<br/>

যেমন - আমাদের নিচের কোডে ৩টা অপারেশন আছে (1 multiplication, 1 addition, 1 division)

```
function sumUpTo (n){
    return n * (n + 1) /2;
}

sumUpTo(10)
```

তাহলে আমরা যদি এই ফাংশনটা রান করতে চাই তাহলে আমাদের এখানে ৩টা অপারেশন রান করছে। এখানে একটা জিনিস লক্ষ্য করার মত হচ্ছে এই অপারেশনগুলো কিন্তু ইনপুটের উপর ডিপেন্ডেন্ট না। এই ফাংশনে আমরা ইনপুট ১০ দেই বা ১০০ দেই বা ১০০০ দেই আমাদের অপারেশন এই ৩টাই থাকবে।

এবার যদি আমরা আমাদের নিচের কোডটিকে দেখি

```
function sumUpTo (n){
    let total = 0;
    for(let i = 1; i <= n; i++>){
        total += i;
    }
    return total;
}
sumUpTo(10)
```

এখানে আমাদের ৫টা অপারেশন চলছে। কিন্তু লুপের ক্ষেত্রে আসলে এভাবে অপারেশন গুনা যায় না। এক্ষেত্রে আমরা যদি ফাংশনে ১০ এর আউটপুট পেতে যাই আমাদের এই অপারেশন গুলো ১০ x ৫ = ৫০ বার, ১০০ এর আউটপুট পেতে হলে ১০০ x ৫ = ৫০০ বার, ১০০০ এর আউটপুট পেতে হলে ১০০০ x ৫ = ৫০০০ বার আমাদের অপারেশনগুলো চলবে। অর্থাৎ আমাদের এই কোডটির অপারেশনগুলো ইনপুটের উপর ডিপেন্ডেন্ট।

<br/>

এই অপারেশন কাউন্ট করে আমরা আমাদের কোডের/আলগরিদমের effieciency measure করতে পারি। কিন্তু এভাবে নির্দিষ্ট করে কাউন্ট করাটা বেশ কঠিন। আমরা যখন বড় বড় কোড লিখবো তখন আসলে এভাবে কাউন্ট করা সম্ভব নয়। এর চাইতে আমাদেরকে ফোকাস করতে হবে আমাদের যে অপারেশন বাড়তেছে এটা কি আকারে বাড়তেছে তার দিকে নজর দেয়া। অর্থাৎ আমার ইনপুট ডাবল করলে আমার অপারেশন কি সেম থাকে নাকি ডাবল হয় নাকি ত্রিপল হয়।