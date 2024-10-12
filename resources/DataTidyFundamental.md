### What is Data Tidy?

**Data Tidy** refers to a systematic and organized approach to structuring data for easy analysis and manipulation. It
follows specific principles that ensure data is arranged in a clear, consistent, and predictable format, making it
easier to work with in data science and analysis tasks.

In tidy data:

- Each **variable** forms a **column**.
- Each **observation** forms a **row**.
- Each **type of observational unit** forms a separate **table**.

Tidy data is a concept championed by **Hadley Wickham**, a key contributor to data science tools in R. However, it is
widely applicable across programming languages like Python, where data is often managed using libraries like Pandas.
Ensuring data is tidy helps streamline analysis and improves efficiency when applying machine learning algorithms or
performing exploratory data analysis.

---

### Fundamentals of Data Tidy

The fundamental principles of data tidying revolve around making data easy to manipulate and analyze. These principles
include:

#### 1. **Each Variable is a Column**

Every variable in your dataset should have its own column. For example, in a dataset of customers, variables such as *
*name**, **age**, and **purchase amount** would each be assigned their own column.

**Example:**
| Name | Age | Purchase Amount |
|-------|-----|-----------------|
| John | 25 | $100 |
| Sarah | 30 | $150 |

#### 2. **Each Observation is a Row**

Every unique observation (record or entity) should be represented by a row. For instance, each customer in the dataset
is a different row, ensuring that each observation is uniquely represented in the data.

**Example:**
| Name | Age | Purchase Amount |
|-------|-----|-----------------|
| John | 25 | $100 |
| Sarah | 30 | $150 |

#### 3. **Each Type of Observational Unit Forms a Table**

Data should be organized into different tables based on the type of observational unit. For example, if you're dealing
with customer data and transaction data, those should be stored in separate tables. Each table represents one type of
information.

**Example (Customers Table):**
| Customer ID | Name | Age |
|-------------|-------|-----|
| 1 | John | 25 |
| 2 | Sarah | 30 |

**Example (Transactions Table):**
| Transaction ID | Customer ID | Purchase Amount |
|----------------|-------------|-----------------|
| 100 | 1 | $100 |
| 101 | 2 | $150 |

#### 4. **Minimal Redundancy**

Tidy data minimizes redundancy and avoids duplication of information across different columns or tables. If certain
details (such as customer age) are needed in multiple contexts, you should reference them through a unique identifier (
such as a customer ID) rather than duplicating the data across different tables.

#### 5. **Consistency in Formatting**

Formatting should be consistent throughout the dataset. If a variable (such as dates or times) is formatted in a
particular way, it should remain consistent across the entire dataset to avoid confusion and ensure data integrity.

#### 6. **Handling Missing Data**

In tidy data, missing values should be handled appropriately. They can either be left as `NaN` (Not a Number) or
represented in a meaningful way that allows for easier analysis without misleading results.

#### 7. **Data Types are Consistent**

Each column should hold values of a consistent type. For example, a column representing numerical data (such as age or
purchase amount) should not contain any strings or text values. Inconsistent data types can lead to errors during
analysis or when applying machine learning models.

---

### Why Tidy Data is Important

**Advantages of Tidy Data:**

1. **Easier Analysis**: Tidy data is structured to be easily manipulated with functions and algorithms, which
   streamlines the data analysis process.
2. **Data Integrity**: By following tidy data principles, you maintain the integrity and consistency of the data,
   minimizing errors or confusion.
3. **Automation**: Tidy data lends itself well to automation and reproducible research, as the structure is predictable
   and manageable.
4. **Compatibility with Tools**: Many data analysis libraries and tools (like **Pandas** in Python or **dplyr** in R)
   are designed to work efficiently with tidy data. This means tidying your data enables more effective use of these
   tools.

---

### Examples of Tidy vs. Untidy Data

#### Untidy Data Example:

| Name  | Age | Purchase 1 | Purchase 2 |
|-------|-----|------------|------------|
| John  | 25  | $100       | $150       |
| Sarah | 30  | $50        | $100       |

In the example above:

- The **Purchase** information is spread across multiple columns, which violates the tidy data principle of each
  variable being its own column.

#### Tidy Data Example:

| Name  | Age | Purchase | Transaction |
|-------|-----|----------|-------------|
| John  | 25  | $100     | 1           |
| John  | 25  | $150     | 2           |
| Sarah | 30  | $50      | 1           |
| Sarah | 30  | $100     | 2           |

In this case:

- Each **purchase** is recorded as a separate row.
- Each **variable** (purchase amount and transaction ID) has its own column, making the data easy to process.

---

### Conclusion

Tidy data principles provide a solid foundation for working with datasets, ensuring consistency, clarity, and efficiency
in data analysis. Adopting these practices early in the data preparation process makes it easier to apply statistical
models, visualize data, and generate insights without spending excess time on restructuring. Whether you are working
with a small dataset or large-scale data, tidying your data is essential for successful analysis.