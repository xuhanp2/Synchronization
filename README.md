This course project uses a Lorenz signal to mask speech and a second Lorenz system with proportional feedback to recover it. The notebook estimates conditional Lyapunov exponents with speech turned off and compares speech recovery with and without a one-second synchronization preamble.

## Run the notebook

Install the Python packages:

```bash
python -m pip install notebook numpy matplotlib tensorflow tensorflow-datasets soundfile
```

Open `SeveralSpeech.ipynb` in Jupyter and run all cells from top to bottom.
The first run downloads the Speech Commands dataset.

## Results

Mean Pearson correlation across ten test recordings at $k=500$:

| Masking factor | Preamble | Mean correlation |
| --- | --- | ---: |
| 0.5 | 1 second | 0.9236 |
| 0.1 | 1 second | 0.5370 |
| 0.5 | None | 0.3144 |