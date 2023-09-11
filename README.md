## llama2.🔥

<p align="center">
  <img src="assets/llama2.mojo-demo.gif" width="700" alt="llama2.mojo logo">
</p>

## why this fork?

This repository serves as a fork that provides a Mojo-based implementation of `llama2.c`.

As it was shown during my experimentations performance of this solution can beat the original `llama2.c` even built
with `runfast` option
Ubuntu virtual machine performance:

| Model           | llama2.py | llama2.c    | llama2.c (runfast) | **llama2.mojo** |
|-----------------|-----------|-------------|--------------------|-----------------|
| stories15M.bin  | 1.3 tok/s | 75.73 tok/s | 237 tok/s          | 260 tok/s       |
| stories110M.bin | -         | 9 tok/s     | 30 tok/s           | 40 tok/s        |

## prerequisites

Make sure you have installed & configured mojo on your environment.
https://docs.modular.com/mojo/manual/get-started/index.html

Or you can use [mojo playground](https://playground.modular.com/) to run this model. 

## feel the 🔥magic

First, navigate to the folder when you keep your projects and clone this repository to this folder:

```bash
git clone https://github.com/tairov/llama2.mojo.git
```

Then, open the repository folder:

```bash
cd llama2.mojo
```

Now, let's just run a baby Llama 2 model on Mojo 

```bash
wget https://huggingface.co/karpathy/tinyllamas/resolve/main/stories15M.bin
```

Just run the Mojo

```bash
mojo llama2.mojo
num hardware threads:  6  SIMD vector width:  8
checkpoint size:  60816028
<s>
Once upon a time, there was a little girl named Lily. She loved to play outside in the sunshine. One day, she saw a big, red ball in the sky. It was the sun! She thought it was so pretty.
Lily wanted to play with the ball, but it was too high up in the sky. She tried to jump and reach it, but she couldn't. Then, she had an idea. She would use a stick to knock the ball down.
Lily found a stick and tried to hit the ball. But the stick was too short. She tried again and again, but she couldn't reach it. She felt sad.
Suddenly, a kind man came by and saw Lily. He asked her what was wrong. Lily told him about the ball. The man smiled and said, "I have a useful idea!" He took out a long stick and used it to knock the ball down. Lily was so happy! She thanked the man and they played together in the sunshine.
<s>
Once upon a time, there was a little girl named Lily. She loved to play outside in the sunshine. One day, she saw a big, red
achieved tok/s:  264.24870466321244
```

## License

MIT