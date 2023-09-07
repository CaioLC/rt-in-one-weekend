# Output an Image

Alright, so we have read Chapter 2 of Ray Tracing in One Week and now we need to create a file. More specifically, our ray tracing code will write pixels to a plain text image format called PPM. PPM expects some metadata in the first few lines and then the pixels are written sequentially, from top to bottom, row by row.

## Step 1: writing anything to a file

Let's create our project with `cargo new raytracing` and start working. First we need some basic IO, to write anything to a text file. Let's checkout `std::io` documentation and see how we can setup this basic task:

```
COPY DOCS HERE
```

Pretty straightfoward. Lets write that directly into our `main()` function.

```
RUST CODE
```

## Step 2: writing a PPM file
