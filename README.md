# Parquet File Compression

Benchmarking columnar storage and compression strategies for large-scale data files using Apache Parquet.

## Overview

This project explores how Apache Parquet's columnar storage format and its supported compression codecs affect file size and I/O efficiency for large datasets. By comparing different storage and compression strategies, it highlights the practical trade-offs involved in storing large-scale data.

## Results

A visual comparison of the benchmarked strategies is available in `compare_results.png`, illustrating the relative file sizes and compression performance across the tested approaches.

## Contents

| Item | Description |
|------|-------------|
| `compare_results.png` | Chart comparing file sizes and compression performance across strategies. |
| `readme_git.rtf` | Supplementary notes documenting the benchmarking process. |

## Requirements

- Python 3.x
- `pyarrow` or `fastparquet`
- `pandas`

Install the typical dependencies with:

```bash
pip install pandas pyarrow
```

## Usage

Read and write Parquet files with different compression codecs to reproduce the comparison, for example:

```python
import pandas as pd

df.to_parquet("data.snappy.parquet", compression="snappy")
df.to_parquet("data.gzip.parquet", compression="gzip")
```

## License

No license has been specified for this repository. Please contact the author before reuse.
