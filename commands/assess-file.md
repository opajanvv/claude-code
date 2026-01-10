# Assess files

Analyze files in the current directory and create assessment reports.

## Instructions

1. First, list all files (not directories) in the current working directory using `ls -lh` to get file sizes and dates.

2. For each file found, spawn a parallel agent (using the Task tool with subagent_type "general-purpose") to analyze the file. Run multiple agents in parallel for efficiency.

3. Each agent should:
   - Read the file content (or examine binary files to determine type)
   - Determine the file type (log, PDF, script, config, data, etc.)
   - Summarize what the content is about
   - Note the file's age based on modification date
   - Provide a recommendation: KEEP, CONSIDER REMOVING, or SAFE TO REMOVE
   - Consider factors like: is it a backup, is it outdated, is it a temporary file, does it contain important data

4. For each analyzed file, create a corresponding `<filename>.assessment.md` file with this format:

```markdown
# Assessment: <filename>

## File information
- **Type:** <file type>
- **Size:** <size>
- **Last modified:** <date>
- **Age:** <how old>

## Content summary
<Brief description of what the file contains>

## Recommendation
**<KEEP | CONSIDER REMOVING | SAFE TO REMOVE>**

<Reasoning for the recommendation>
```

5. After all agents complete, provide a summary of findings to the user.

## Notes

- Skip directories - only assess regular files
- For binary files (PDFs, images), describe based on filename and metadata
- For large files, read only the first portion to understand content
- Be conservative with "SAFE TO REMOVE" - only suggest this for clearly temporary or redundant files
