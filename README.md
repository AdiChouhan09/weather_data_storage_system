# Weather Data Storage System  

## **Overview**  
Implementation of a Weather Data Storage System using Abstract Data Types (ADTs) and 2D arrays.  
Supports insertion, deletion, retrieval, row-major & column-major access, sparse data handling,  
and time/space complexity analysis.  

---

## **1. Weather Record ADT Design**  

**Attributes:**  
- **Date:** Either a structured format (day/month/year) or a string (YYYY-MM-DD).  
- **City:** The city's name in string form.  
- **Temperature:** The recorded temperature represented by a floating-point number.  

**Methods:**  
- **insert(data):** Update the system with a new weather entry.  
- **delete(data):** Remove a weather record according to parameters like date and city.  
- **retrieve(city, year):** Retrieve all temperature records for a given city and year.  

---

## **2. Data Storage Class Design**  

**Attributes:**  
- **2D Array:** A table-like structure where each column represents a city and each row represents a year.  

**Methods:**  
- **populateArray():** Set up and add temperature data to the 2D array.  
- **rowMajorAccess():** Sequential access row by row.  
- **columnMajorAccess():** Sequential access column by column.  
- **handleSparseData():** Use sparse storage or sentinel values (e.g., NaN) to manage incomplete datasets.  
- **analyzeComplexity():** Report time and space complexity of main operations.  

---

## **3. Method of Implementation**  

**a. Row-Major vs Column-Major Access**  
- **Row-Major:** Access all elements in the current row before moving to the next row.  
- **Column-Major:** Access all elements in the current column before moving to the next column.  

**Observation:** Efficiency depends on whether row-wise or column-wise queries predominate.  

**b. Managing Sparse Data**  
- **Sentinel Values:** Use placeholders (e.g., `-1` or `None`) to indicate missing data.  
- **Sparse Matrix Representation:** Store only valid entries with row and column indices to reduce memory overhead.  

---

## **4. Time and Space Complexity Analysis**  

**Time Complexity (Key Operations):**  

| Operation   | Row-Major | Column-Major |
|-------------|-----------|--------------|
| **Insert**  | O(1)      | O(1)         |
| **Retrieve**| O(n × m)  | O(n × m)     |
| **Delete**  | O(n × m)  | O(n × m)     |

**Space Complexity:**  
- **Dense 2D Array:** O(n × m) (memory allocated for all entries, even empty ones).  
- **Sparse Matrix:** O(k), where *k* is the number of valid records only.  

---

## **Screenshot**  
Below is the sample output of the program execution:  

<img width="1188" height="240" alt="Screenshot 2025-10-01 201111" src="https://github.com/user-attachments/assets/9ae1dc29-e099-420f-bec8-1d954c8f5cda" />
  
---

## **Author**  
- **Name:** Aditya Chouhan  
- **Roll No:** 2401830001  
- **Course:** B.Sc. (H) Cybersecurity  

