# Structured AI Data Framework – User Stories & Implementation Guide

## [UR-01] Structured Training Data Framework

**User Story:**  
As a developer, I want to implement a structured training data framework so that I can categorize and retrieve data efficiently.

**Purpose:**  
After talking to the client, they expressed the need for structured and easily accessible training data. They find it difficult to work with unorganized datasets, which affects AI training performance. The decision was made to build a framework using a relational database (e.g., IBM Db2) to separate and categorize training questions from answers.

**Implementation Strategy:**
- Use IBM Db2 as the database management system.
- Store training questions and answers separately.
- Implement efficient retrieval queries.

### 🔴 Priority: High

### Sub-Issues

#### [UR-01.1] Create a Table for Training Questions
- **Assumption:** Structured training questions improve retrieval efficiency.
- **Validation:** Verify that the training questions table is created and can store sample data.
- **Tasks:**
  - Create a table with `question_id`, `question_text`, `category`, `created_at`.
  - Set `question_id` as the primary key.
  - Execute SQL script and verify the table structure.

#### [UR-01.2] Create a Table for Training Answers
- **Assumption:** Answers should be linked to their respective questions.
- **Validation:** Ensure a JOIN query can retrieve the correct answers for questions.
- **Tasks:**
  - Create a table with `answer_id`, `question_id`, `answer_text`, `created_at`.
  - Set `question_id` as a foreign key referencing `training_questions`.
  - Verify relationships with sample queries.

#### [UR-01.3] Implement SQL Queries for Retrieval
- **Assumption:** Developers need quick access to categorized questions and answers.
- **Validation:** Ensure queries return accurate results in minimal time.
- **Tasks:**
  - Write SQL queries to fetch categorized questions and answers.
  - Optimize queries for performance.
  - Validate results with test data.

---

## [UR-02] Bias-Checking Tool

**User Story:**  
As a developer, I want to build a tool that checks for bias in training data so that my AI models can be fair.
