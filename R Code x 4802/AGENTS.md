# Introductory R Class Instructions

- This project is for an introductory-level R coding class using RStudio.
- Use R by default and assume all code will be run in RStudio.
- Provide complete, runnable code.
- Explain the code step by step in plain language.
- Avoid advanced shortcuts unless you explain them.

# Amanda's R Style

## Document Format and Structure

- Use R Markdown (`.Rmd`) for analysis and lesson documents, with a standard YAML header containing `title`, `author`, `date`, and `output: html_document`.
- Organize major sections with `# Learning Outcomes:`, topics with `##`, subtopics with `###`, and concrete operations or examples with `####`.
- For each concept, put explanatory Markdown text outside code chunks, followed by minimal R code chunks using the standard opening fence of three backticks followed by `{r}` and a closing fence of three backticks.
- End sections with numbered practice exercises (`1.`, `2.`, and so on).

## Naming Conventions

- Use `lowerCamelCase` for objects, vectors, data frames, and functions, such as `cookieDat`, `earlyToClass`, `tvShows`, and `chickEight`.
- Data frame column names are flexible. Default to original dataset names, or transform them to all lowercase or uppercase using `tolower()` or `toupper()`.

## Syntax and Operator Preferences

- Always use `<-` for object assignment. Never use `=` to store variables; reserve `=` for function argument binding.
- Both native R pipes (`|>`) and tidyverse pipes (`%>%`) are acceptable.
- Always show base R methods first before providing tidyverse alternatives:
  - Create vectors with `c()`, `seq()`, `rep()`, and `1:N`.
  - Use `cbind.data.frame()` and `rbind.data.frame()` for combining data frames.
  - Show matrix-style indexing (`df[df$col==val, ]`) and `subset(df, condition)` before `dplyr::filter()` or `dplyr::select()`.
- Add inline comments for interactive-only functions, for example `?mtcars # only do this in the console`.

## Functions and Logic

- Define custom functions using standard assignment:

```r
functionName <- function(arg1, arg2) {
  # body
}
```

- Use vectorized `ifelse(condition, true, false)` for column creation or mutations, or standard `for(i in 1:nrow(df))` loops for row-wise iteration.

## Code Spacing and Subsetting

- Use compact spacing around mathematical and logical operators, such as `5*7<=30`, `3^5>sqrt(10000)`, and `df$col==0`.
- Prefer explicit column extraction with `$` notation (`df$col`) or index positioning (`df[, 1]`).
