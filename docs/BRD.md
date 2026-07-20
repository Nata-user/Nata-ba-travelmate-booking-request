

# **Business Requirements Document(BRD) Template**

## *Project/Initiative*

## *Month 20YY*

## *Version X.XX*

*Company Information*

1. # **Document Revisions**

| Date | Version Number | Document Changes |
| ----- | ----- | ----- |
| 05/02/20xx | 0.1 | Initial Draft |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

2. # **Approvals**

| Role | Name | Title | Signature | Date |
| ----- | ----- | ----- | ----- | ----- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

3. # **Introduction**

   1. ## **Project Summary**

      1. ### **Objectives**

   *Provide users with the ability to quickly find hotels based on city, dates, and other search criteria, simplifying the process of selecting the most suitable accommodation option.* 

      2. ### **Background**

   *\[Provide a brief history of how the project came to be proposed and initiated, including the business issues/problems identified, and expected benefit of implementing the project/developing the product.\]*

   

 


         1. #### ***Business Drivers***

   *\[List the business drivers that make development of this product important. These can be financial, operational, market or environmental.\]* 

2. ## **Project Scope**

   *The project covers the hotel search and filtering process, from entering the city and stay dates to viewing search results, applying filters, and selecting a specific hotel from the list. The scope does not include booking, payment processing, or user profile management.* 

   1. ### **In Scope Functionality**

1. Hotel search by destination, dates, and guests.  
2. Destination autocomplete.  
3. Hotel details display.  
4. Filtering by price, rating, free cancellation, and amenities.  
5. Recommended hotels and marketing tags.  
6. Input validation.  
7. Search statistics collection.  
8. Responsive design.

   

   2. ### **Out of Scope Functionality**

1. Payments.  
2. User accounts and booking history.  
3. Favorites.  
4. User reviews.  
5. Map-based search.  
6. Discounts.  
7. Multi-language and multi-currency support.  
8. Any functionality not listed in the In Scope section

   

   

   3. ## **System Perspective**

   *\[Provide a complete description of the factors that could prevent successful implementation or accelerate the projects, particularly factors related to legal and regulatory compliance, existing technical or operational limitations in the environment, and budget/resource constraints.\]*

      1. ### **Assumptions**

      2. ### **Constraints**

* 

  3. ### **Risks**

*   
* .

  4. ### **Issues**

* 


4. # **Business Process Overview**

   *\[Describe how the current process(es) work, including the interactions between systems and various business units. Include visual process flow diagrams to further illustrate the processes the new product will replace or enhance.*

   *Use case documentation and accompanying activity or process flow diagrams can be used to create the description(s) of the proposed or “To-Be” processes.\]*

   1. ## **Current Business Process (As-Is)**

At any point during or after deployment of web apps or web sites (internal or external) to support business activities, development/support teams may create and deploy widgets. 

1. CMS / database administrators for the employee portal use the CMS tool to create widgets. They can test widgets in the designated staging environment, then register them and deploy to production.  
2. Development teams may deploy widgets to development and testing environments set up for their development projects. They must check widget code into and out of the source code repository according to their projects’ development schedule.  
   ![][image1]

   2. ## **Proposed Business Process (To-Be)**

1. Technical Lead searches repository   
2. If widget is not found, user creates a new widget name record.  
3. WINS validates that all fields have been completed.  
4. WINS confirms that no similar widgets exist  
5. User confirms record to be created.  
   ![][image1]  
1. User searches repository to locate existing widget description.  
2. WINS displays record  
3. User selects Edit to open and modify record  
4. WINS validates all fields completed correctly  
5. User confirms changes.  
6. WINS confirms changes and updates Audit table.

   ![][image1]

5. # **Stakeholder Requirements**

   *\[The specific user requirements elicited from stakeholders should be listed, categorized by both priority and area of functionality to smooth the process of reading and tracking them. Include links to use case documentation, and other key reference material as needed to make the requirements as complete and understandable as possible.  You may wish to incorporate the functional and non-functional requirements into a traceability matrix that can be followed throughout the project.\]* 

The requirements in this document are prioritized as follows:

| Value | Rating | Description |
| ----- | ----- | ----- |
| 1 | Critical | The system should allow you to search for your own venues by city, dates, and number of guests.  |
| 2 | High | The system should support city auto-completion and fast search (up to 2 seconds).  |
| 3 | Medium | The system must support viewing results on a map.  |
| 4 | Low | The system should display marketing tags ("Best Price", "1 room left"). |
| 5 | Future | The system must support multiple languages ​​and currencies.  |

1. ## **Functional Requirements**

| Req\# | Priority | Description | Rationale | Use Case Reference | Impacted Stakeholders |
| ----- | :---: | ----- | ----- | ----- | ----- |
| **General / Base Functionality** |  |  |  |  |  |
| FR-G-001 | 1 | The system shall allow users to search hotels by destination city.  | Supports the main search process.  | UC-01 Search Hotels  | Customers, Business Owner  |
| FR-G-002 | 2 | The system shall provide an autocomplete suggestion list when the user enters a destination city.  | Improves search speed and usability.  | UC-01 Search Hotels  | Customers |
| FR-G-003 | 1 | The system shall allow users to select check-in and check-out dates using a calendar.  | Supports the main search process.  | UC-01 Search Hotels  | Customers |
| FR-G-004 | 3 | The calendar shall visually distinguish weekends from weekdays.  | Improves calendar usability.  | UC-01 Search Hotels  | Customers |
| FR-G-005 | 1 | The system shall allow users to specify the number of adult guests. | Ensures accurate hotel search and pricing.  | UC-01 Search Hotels  | Customers, Business Owner  |
| FR-G-006 | 1 | The system shall allow users to specify the number of children.  | Ensures accurate hotel search and pricing.  | UC-01 Search Hotels  | Customers, Business Owner  |
| FR-G-007 | 1 | The system shall allow users to specify the age of each child.  | Ensures accurate child pricing.  | UC-01 Search Hotels  | Customers, Business Owner  |
| FR-G-008 | 1 | The system shall use the selected destination, check-in date, check-out date, number of guests, and the age of each child to search for available hotels. | Ensure accurate search results.  | UC-01 Search Hotels  | Customers, Business Owner  |
| FR-G-009 | 1 | The system shall use the number of guests and the age of each child to calculate the total accommodation price for the selected stay.  | Ensure accurate price calculation.   | UC-02 View Hotel Details  | Customers, Business Owner  |
| FR-G-010 | 1 | The system shall display available hotels matching the search criteria.  | Enables hotel selection.  | UC-01 Search Hotels  | Customers  |
| FR-G-011 | 2 | The system shall allow users to filter hotels by price range by specifying minimum and maximum prices.  | Improves search accuracy.  | UC-02 Filter Hotels  | Customers  |
| FR-G-012 | 2 | The system shall allow users to filter hotels by minimum guest rating. | Improves search accuracy.  | UC-02 Filter Hotels  | Customers  |
| FR-G-013 | 2 | The system shall allow users to filter hotels that offer free cancellation. | Improves search accuracy.  | UC-02 Filter Hotels  | Customers  |
| FR-G-014 | 2 | The system shall allow users to filter hotels by one or more amenities (e.g., Wi-Fi, parking, swimming pool, breakfast, air conditioning). | Improves search accuracy.  | UC-02 Filter Hotels  | Customers  |
| FR-G-015 | 2 | The system shall allow users to apply multiple filters simultaneously. | Enables more precise search results. .  | UC-02 Filter Hotels  | Customers  |
| FR-G-016 | 1 | The system shall update the search results based on the selected filters. | Ensures search results reflect the selected filters.   | UC-02 Filter Hotels  | Customers  |
| FR-G-017 | 1 |  The system shall display hotel details including photos, rating, total price for the entire stay, and distance from the city center.  |  Helps users compare and select hotels.   |  UC-03 View Search Results  |  Customers  |
| FR-G-018 | 2 | The system shall display recommended hotel offers based on predefined business rules.  | Supports promotion of business-priority hotel offers.  | UC-03 View Search Results  | Customers, Business Owner  |
| FR-G-019 | 2 | The system shall highlight selected hotel offers with marketing tags (e.g., "Only 1 room left", "Best Price"). | Increases the visibility of promoted hotel offers.  | UC-03 View Search Results  | Customers, Business Owner  |
| FR-G-020 | 2 | The system shall prioritize recommended offers in the search results without excluding hotels that match the user's search criteria. | Supports business goals by prioritizing promoted offers.  | UC-03 View Search Results  | Customers, Business Owner  |
| FR-G-021 | 2 |  The system shall allow users to switch between list view and map view of search results.  |  Improves location-based  hotel selection.  |  UC-04 View Hotels on Map  |  Customers  |
| **Security Requirements** |  |  |  |  |  |
| FR-S-001 | 1 |  The system shall validate all user inputs before processing the search request. If validation fails, the system shall display a clear validation message indicating the invalid field and the reason for the error.   | Prevents invalid requests and attacks.  | UC-01 Search Hotels  | Customers, IT Team  |
| **Reporting Requirements** |  |  |  |  |  |
| FR-R-001 | 2 |  The system shall provide administrators with access to aggregated hotel search statistics.   |  Supports business analysis.  |  UC-01 Search Hotels  |  Business Owner  |
|  **Usability Requirements** |  |  |  |  |  |
|  |  |  |  |  |  |
| **Audit Requirements** |  |  |  |  |  |
| FR-A-001 | 1 | The system shall log each search request, including the destination, check-in and check-out dates, number of guests, applied filters, and search timestamp.   |  Supports monitoring and troubleshooting.  |  UC-01 Search Hotels  | Business Owner, IT Team |
| FR-А-001 | 1 |  The system shall display the search  results after processing a valid search  request.   |  Improves user experience.  |  UC-01 Search Hotels  |  Customers  |

   2. ## **Non-Functional Requirements**

   *\[Include technical and operational requirements that are not specific to a function. This typically includes requirements such as processing time, concurrent users, availability, etc.\]*

| ID | Requirement |
| ----- | ----- |
| NFR-001 | The system shall display search results within **2 seconds** for 95% of search requests.  |
| NFR-002 | The system shall support at least **1,000 concurrent users** without performance degradation.  |
| NFR-003 | The system shall maintain **99.9% availability** excluding scheduled maintenance.  |
| NFR-004 | The system shall update hotel availability data within **5 seconds** after receiving changes from external providers.  |
| NFR-005 | The system shall support responsive design for screen widths from 320 px to 1920 px. The application shall display and function correctly in the latest two versions of Chrome, Edge, Firefox, and Safari on desktop and mobile devices. .  |

6. # **Appendices**

   1. ## **List of Acronyms**

   *\[If needed, create a list of acronyms used throughout the BRD document to aid in comprehension.\]*

   2. ## **Glossary of Terms**

   *\[If needed, identify and define any terms that may be unfamiliar to readers, including terms that are unique to the organization, the technology to be employed, or the standards in use.\]*

   3. ## **Related Documents**

   *\[Provide a list of documents or web pages, including links, which are referenced in the BRD.\]*

[image1]: <data:image/png;base64,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>


