# ai-digest composite action

This action runs the [ai-digest](https://github.com/khromov/ai-digest) CLI to aggregate file content into a single Markdown file.

## Why

AI tools such as [Codeium](https://codeium.com/) can be passed a text file in a format such as `Markdown` or `JSON` that adds [context](https://codeium.com/context) to the tool's chat responses and code completions.

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
uses: actions/ai-digest
with:
  input_path: './docs'
  output_file: 'docs.md'
  digest_log: 'ai-digest-log.md'
```
