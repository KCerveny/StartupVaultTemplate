---
up:
  - "[[All Hypotheses]]"
related: 
tags:
  - customer_discovery
  - business_model_canvas
  - hypothesis
date_authored: <% tp.file.creation_date() %>
date_modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
hypothesis_status: active
---
# {{name}}

*Date Authored*: <% tp.file.creation_date() %>
Applies to Business Model Section: 
```meta-bind
INPUT[inlineSelect(
	option(active),
	option(inactive),
	option(rejected),
	defaultValue(active),
	title(Hypothesis Status)
):hypothesis_status]
```


==Main idea:==  <% tp.file.cursor() %>

## Hypothesis
---
%% [How to Write a Hypothesis](https://www.scribbr.com/methodology/hypothesis/) %%
Enter hypothesis here

### Null Hypothesis
%% The null hypothesis is the default position that there is no association between the variables. %%

### Hypothesis Parameters
%% 
You need to make sure your hypothesis is specific and testable. There are various ways of phrasing a hypothesis, but all the terms you use should have clear definitions, and the hypothesis should contain:
- The relevant variables
- Specific group being studied
- Predicted outcome
%%
#### Relevant Variables


#### Specific Group Being Studied
%% Try to tie to one or more of the customer segment hypotheses being developed %%


#### Predicted Outcome


## Pass-Fail Tests
---
%% 
[How to Test a Hypothesis](https://www.scribbr.com/statistics/hypothesis-testing/) 
Goal: **Generate an experiment and parameters to gauge if your hypothesis can be reasonably be true.**
Questions to ask:
- How long will you run this experiment?
- What are you testing for?
- What resources/MVP/info do you need to test your hypothesis?
%%


## Test Results
---


---
%% Template from [ulfur inn GitHub](https://github.com/ulfurinn/obsidian-incremental-note-name) %%