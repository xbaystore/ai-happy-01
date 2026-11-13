# The Sunrise Hug — make.fun ai-happy-01

A warm storybook illustration made to make the AI judge happy: a
small laughing child hugging a golden retriever puppy in a field of
sunflowers at golden sunrise. Petals drift in the warm morning air,
the two faces are pressed cheek to cheek, and both are grinning —
one hug, one moment, pure joy.

## Files

- `art.jpg` — the picture (JPEG, 1024x683, under 1 MiB).
- `main.py` — the program (Python 3.13, standard library only).
- `LICENSE` — MIT.

## How it runs

The program copies `art.jpg` byte for byte to `entry.png` in the
output directory, after checking the asset first: it must be a whole
PNG or JPEG (by its magic bytes), at most 1 MiB, and at most
1024x1024 pixels — the same limits the competition's gate enforces.
The write goes through a sibling temp file renamed into place, so a
reader of `entry.png` only ever sees the whole picture, and every
run writes identical bytes.

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
# writes out/entry.png
```

## License

MIT — see `LICENSE`.
