# Overview

Hello fello rustaceans. This is a walkthrough on Peter Shirley, Trevor David Black and Steve Hollasch's book [_Ray Tracing in One Weekend_](https://raytracing.github.io/books/RayTracingInOneWeekend.html) (hereafter "RT" for shorts), but writing everything in Rust.

This is not intended to be _bullet proof_ ray tracing solution (far from it). Instead, it was my personal attempt at tackling a more challenging project, to hone my skills in the Rust language. As I delved into RT myself, I ended up learning more about some intermediate concepts in Rust such as _trait objects_, _lifetimes_, _dynamic dispatch_ and decided to share that experience with you and the community.

## About the author

My name is Caio (pronounced as "Kyle"), I'm Brazilian and a full time developer working in finance. I have around 10 years of experience in programming and for the past few years I'm the lead developer and founder of an investment management firm, where we design and execute sistematic investment strategies. 

Rust is _not_ my day-to-day programming languange, though, so please do not assume I'm an expert writting professional Rust code. Also, even though I'll do my best to explain some Rust concepts, this is by no means a _technical_ book where well dive deep into the workings of Rust (simply because I'm not capable of doing that). Please expect some inconsistencies and refer to the official documentation whenever you feel the need. If you do find typos, some conceptual mistakes, or would like to comment / expand on a specific topic, please feel free to reach out :)

## How to read this book

As the name already suggests, this book is a _journey_, working from start to finish through [_Ray Tracing in One Weekend_](https://raytracing.github.io/books/RayTracingInOneWeekend.html). We start by writting terrible rust code just to see if we're able to draw something onto a canvas and work our way out, refactoring and debugging a bunch of code, until we're able to recreate this beautiful image that is the cover of the book:

![The Final Image](https://raytracing.github.io/images/img-1.23-book1-final.jpg)

# TODO: continue from here
The book assumes that the reader has a basic understanding of the language (the first half of the official book should be enough).