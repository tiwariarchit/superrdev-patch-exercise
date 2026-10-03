# Patch Notes

## Summary of Changes

I reviewed the frontend, Spring Boot backend, and database-related code and focused on issues affecting task retrieval and user-visible performance.

* Fixed the task search/filtering logic so the search query is correctly applied when retrieving tasks.
* Removed an artificial delay from the task retrieval flow that unnecessarily slowed down API responses.
* Kept the existing application structure, API endpoints, and startup commands unchanged.

The changes were intentionally kept small and focused rather than restructuring the application.

## What I Did Not Change

I did not rewrite the frontend or backend architecture, change the database technology, or modify unrelated parts of the application. I also did not make broad UI or styling changes because they were outside the highest-value bugs I identified during the timebox.

## Biggest Remaining Risk

The main remaining risk is limited automated test coverage around combinations of search, status filtering, pagination, and API responses. More comprehensive integration tests would make regressions in these areas easier to detect.

## Tools / AI Used

I used ChatGPT to help review the code, understand the existing request flow, identify potential bugs, and reason about possible fixes. I manually reviewed the suggested changes, applied the relevant changes to the project, and verified the implementation rather than blindly copying generated code.
