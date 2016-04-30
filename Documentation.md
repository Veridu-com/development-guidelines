# Documentation

## Internal
You MUST NOT document simple macros or functions, be as smart about your documentation as you are about your code.

Usually method/function documentation in terms of **parameters** and **return** values, along with a **short description** are often good enough.

Add comments for complex code segments but avoid obvious comments.

## External
You are not supposed to write a paper or a book on your project, specially because nobody will ever read it if it is too long (you know, people have better things to do than read very long dissertations on whatever), but your MUST ensure that whoever tries to RUN, EXTEND or REVIEW your project, have a clear idea of:
- WHAT IT DOES: Nobody will be tested on what your project does, so be assertive and clear
- HOW IT DOES: Nobody will major on your project either, so keep it simple, add whatever details are needed but bear in mind who is your audience
- WHAT IT NEEDS TO RUN: Assume people are executing your project on a clean environment and they need a step-by-step guide, also assume that whoever is trying to run your project may NOT have any knowledge of your project's stack and may not even have experience with the language you use in it
- HOW TO EXECUTE IT: Again, people need a step-by-step guide to execute your project and may lack experience, so be kind in the details

### Requirements
You MUST provide a `README.md` file with your project with the above questions detailed in it.

You MAY provide an extended documentation with details that are meant for a more experienced or even a specific audience, such as data people or system administrators etc.
