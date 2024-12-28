# GPU Memory Calculator for LLMs

This is a web-based tool designed to calculate the approximate GPU memory required to serve Large Language Models (LLMs) based on the number of model parameters and quantization bits. It provides an easy way to estimate memory requirements without the need for manual calculations, offering a quick and intuitive solution for AI practitioners.

## Features

- **Parameter Input**: Enter the number of parameters (in billions) for your model.
- **Quantization Selection**: Choose from various quantization bit options (e.g., 2-bit, 4-bit, FP16, FP32, etc.).
- **GPU Memory Calculation**: Get an approximate GPU memory requirement instantly.

---

## How to Use

1. Go to: https://alex188dot.github.io/GPU-VRAM-Calculator
2. Enter the number of parameters for your LLM (in billions)
3. Select the desired quantization (e.g., 8-bit or 16-bit)
4. Click on the "Calculate" button
5. The estimated GPU memory requirement will be displayed below the form

---

## Formula

The memory requirement calculation uses the following formula:

```
Memory Requirement (GB) = (Parameters × Quantization Bits / 8) × 1.2
```

Where:

- Parameters: The actual number of model parameters (converted from billions)
- Quantization Bits: The number of bits used for parameter quantization
- 8: Represents the number of bits per byte
- 1.2: An overhead factor of 20%, accounting for additional memory usage

## Explanation

### Components Breakdown

1. **Parameters**

   - This is the total number of parameters in your model
   - If your model size is in billions, multiply by 1,000,000,000 to get the actual count

2. **Quantization Bits**

   - The number of bits used to represent each parameter
   - Common values are 16 (FP16), 8 (INT8), or 4 (INT4)

3. **Bits per Byte Conversion**

   - Division by 8 converts the result from bits to bytes

4. **Overhead Factor**
   - Multiplication by 1.2 accounts for additional memory requirements
   - This includes memory needed for optimization, gradients, and other runtime requirements

## Example Usage

For a model with:

- 1 billion parameters (1,000,000,000)
- 16-bit quantization

The calculation would be:

```
Memory (GB) = (1,000,000,000 × 16 / 8) × 1.2
```

Result

```
2.24 GB
```

---

## Disclaimer

This tool provides approximate GPU memory requirements and is intended for quick estimations. Actual requirements may vary due to factors like:

- Model architecture
- GPU-specific features (e.g., memory bandwidth, teraflops)
- Additional memory usage by model implementations

---

## Technical Details

Built with plain HTML, CSS and JS

## Support

Feel free to star this repo and share it with others!

If you find this tool helpful, tips are appreciated! Here are the crypto wallets for donations:

- **SOL**: `G2XEByVSfa7qjY9kiD1717Js1fXjM144oh6ngsv912R5`
- **BTC**: `bc1qp9wgx86fn4zu2rp6u09rkw22dlyrxpf5ewsngu`
- **ETH**: `0x0eB9792F58e3eCbf280C213911022f6860D7bcD8`

---

## License

This project is open-source and available under the Apache-2.0 license.

Thank you for using the **GPU Memory Calculator for LLMs**!
