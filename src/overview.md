# Overview

Hello fellow rustaceans! This is a walkthrough on Peter Shirley, Trevor David Black and Steve Hollasch's book [_Ray Tracing in One Weekend_](https://raytracing.github.io/books/RayTracingInOneWeekend.html), but writing everything in Rust 🦀. 

For those who don't know, Ray Tracing in One Weekend is an introductory book about, well... ray tracing, a rendering technique used to generate images by tracing the path of light from a camera through a 2D viewing plane. It can provide great degree of realism (real-world reflections, refractions, shadows, etc.) at a greater computation cost when compared to other rendering techniques such as rasterization.

The original book provides thorough explanation of ray tracing fundamentals and the corresponding code implementation written in C++. We will be following along, adapting the original C++ code to Rust and learning a few things along the way. 

By the end of this journey, we will have a Rust implementation for using ray tracing to draw objects on a canvas. Needless to say this is not intended to be a professional, _bullet proof_, ray tracing solution (far from it). Instead, it is my personal attempt at tackling a more challenging project, and honing my skills in the Rust language. As I delved into the book myself, I ended up learning more about some intermediate concepts in Rust such as _trait objects_, _lifetimes_, _dynamic dispatch_ and others, and decided to share that experience with you and the community.

## About the author

My name is Caio (pronounced as "Kyle"), I'm Brazilian and a full time developer working in finance. I have around 10 years of experience in programming and for the past few years I'm the lead developer and founder of an investment management firm, where we design and execute sistematic investment strategies. 

Most of my experience though is with Python and Rust is _not_ my day-to-day programming languange. I use the latter mostly for hobby projects (some CLI, some automations and some games I never finish...), and I would consider myself at a beginner-to-intermediate level. Please do not assume I'm an expert writting professional Rust code (which I am not) and take everything I say with a grain of salt :).

## How to read this book

As the name already suggests, this book is a _journey_, working from start to finish through [_Ray Tracing in One Weekend_](https://raytracing.github.io/books/RayTracingInOneWeekend.html). We start by writting terrible Rust code just to see if we're able to draw something onto a canvas and work our way out, refactoring and debugging a bunch of code, until we're able to recreate this beautiful image that is the cover of the book:

![The Final Image](https://raytracing.github.io/images/img-1.23-book1-final.jpg)

This book assumes that the reader has a basic understanding of Rust (the first half of the official [book](https://doc.rust-lang.org/stable/book/title-page.html) should be enough) and has played with the language with a few toy projects at least. When we encounter some more intermediate / advance concepts, such as dynamic dispatch and lifetimes, I'll do my best in explaining how they work and why we need them to our use case. Again, I'm definitely not an expert in such matters, so feel free to reach for the official docs or to correct me on some misconceptions whenever needed.

Also, this is not a complete re-write of _Ray Tracing in One Weekend_. We'll go through it, chapter by chapter and make references to the content, but the reader is expected to read the chapters as well, as I will focus solely on translating the C++ code to Rust and not on explaining how ray tracing actually works.

Ok, enought foreword and disclaimers. Let's checkout what ray tracing is all about.
