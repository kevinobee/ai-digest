# ai-digest action

GitHib Action to run [ai-digest](https://github.com/khromov/ai-digest) CLI. Aggregate multiple files into a single `Markdown` file and add it your AI tool of choice. 

By adding context to an AI tool you enable it to generate more accurate chat responses and code completions for any subject domain.

[![Test](https://github.com/kevinobee/ai-digest/actions/workflows/test.yml/badge.svg?branch=main)](https://github.com/kevinobee/ai-digest/actions/workflows/test.yml)

## Inputs

### `input_path`

**Optional** The input directory to aggregate content from (default: current directory).

### `output_file`

**Optional** Specify output file (default: codebase.md).

### `digest_log`

**Optional** Specify digest log file (default: ingest.md).

### `ai_digest_flags`

**Optional** Flags passed to `ai-digest` (default: '--whitespace-removal --show-output-files').

## Outputs

### `total_files`

Total number of files parsed from the `input_path` folder.

### `included_files`

Total number of files included in the output file.

### `ignored_files`

Total number of files ignored.

### `binary_files`

Total number of binary files in the output file.

### `estimated_tokens`

Estimated number of tokens in the output file.

## Example usage

```yaml
uses: kevinobee/ai-digest
with:
  input_path: './docs'
  output_file: 'docs.md'
  digest_log: 'ai-digest-log.md'
```
