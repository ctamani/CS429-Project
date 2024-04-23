# CS429-Project
<h2> Abstract </h2>
The project aims to develop a scalable and efficient web crawling, indexing, and query processing system using Python technologies such as Scrapy, Scikit-Learn, and Flask. The system includes a Scrapy-based web crawler for downloading web documents in HTML format, a Scikit-Learn-based indexer for constructing an inverted index with TF-IDF score/weight representation and cosine similarity, and a Flask-based processor for handling free text queries in JSON format. The primary objectives of the system are to provide efficient content retrieval and query processing capabilities. 

As for the next steps, the project aims to enhance the components. The crawler could implement concurrent and distributed crawling, the indexer might use vector embedding and semantic search, and the processor could integrate query spelling correction and expansion. Evaluating performance on large-scale datasets is also crucial. 

In summary, this basic implementation sets the stage for a robust web document retrieval system and knowledge exploration tool.

<h2> Overview </h2>
The solution consists of three main components: a web crawler, an indexer, and a query processor. The web crawler is responsible for fetching web documents, the indexer constructs an inverted index for efficient search, and the query processor handles user queries and returns relevant results. This proposed system aims to provide a robust solution for content retrieval and query processing tasks.

<h2> Design </h2>
    <ol>
        <li><strong>Web Crawler:</strong><ul>
            <p>Implemented using Scrapy, the crawler fetches web documents starting from a seed URL, allowing for the specification of maximum pages and depth for crawling. It supports concurrent crawling for faster retrieval of web content and is designed to handle large-scale crawling tasks efficiently.</p>
            </ul></li>
        <li><strong>Indexer:</strong><ul>
            <p>Uses Scikit-Learn's TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer to build an inverted index, enabling efficient search based on cosine similarity. It also stores the inverted index in a pickle format for easy retrieval and updating.</p></ul></li>
        <li><strong>Query Processor:</strong><ul>
            <p>Implements a Flask application to process user queries in json format, providing query validation and returning top-K ranked results based on the indexed documents.</p></ul></li>
    </ol> 
    <p>Each document operates independently, which enables flexibility and scalability in the management of the system.</p>


<h2> Architecture </h2>
The system architecture includes:
-  A Scrapy-based crawler for content retrieval.
-  A Scikit-Learn-based indexer for constructing an inverted index.
-  A Flask-based processor for handling user queries.
These components interact via well-defined interfaces, exchanging data in the JSON format. This system was implemented using Python 3.10+, Scrapy 2.11+, Scikit-Learn 1.2+, and Flask 2.2+ libraries.

<h2> Operation </h2>
The system is operated by running the provided Python scripts. The web crawler can be initiated with seed URLs, maximum pages, and maximum depth parameters. The indexer requires adding documents to build the inverted index. As for the query processor, send user queries in JSON format to the specified endpoint.

<h2> Conclusion </h2>
The project successfully implements a web crawling, indexing, and query processing system using Python. The system provides efficient content retrieval and query processing capabilities. Future steps include enhancing scalability and incorporating features such as query expansion and spelling correction.

<h2> Data Sources </h2>
The system does not use external data sources, it's designed to crawl and index web documents from any publicly accessible website. In this case, the URLs used were from explainxkcd.com, en.wikipedia.org, and scienceofpeople.com.


<h2> Test Cases </h2>
Test cases were implemented to validate the functionality of each component, including adding documents, processing queries, and handling edge cases and errors.

Crawler:
Purpose: Evaluate crawler behavior when crawling different websites.
Framework: Scrapy testing framework.
Harness: Scrapy test harness for spider-based tests.
Coverage: Comprehensive testing of crawling behavior on different websites.

Processor:
Purpose: Validate the functionality of adding documents and processing queries.
Test Steps: Send requests to add documents and query the system, then verify the responses.
Framework: Python unittest framework.
Harness: Flask's test client for simulating HTTP requests.
Coverage: Ensures the processor handles document addition, query processing, and error cases correctly.

Indexer:
Purpose: Verify the functionality of adding documents, building the index, and performing searches.
Test Steps: Add documents, build the index, and perform searches, then verify the results.
Framework: Python unittest framework.
Harness: Test environment for adding documents and building the index.
Coverage: Testing document addition, index building, search functionality, and TF-IDF matrix accuracy.

<h2> Source Code </h2>
The source code for this project was produced using OpenAI's ChatGPT model.

<h2> Bibliography </h2>
    <p>Manning, Christopher D., Prabhakar Raghavan, and Hinrich Schütze. <em>An introduction to information retrieval.</em> Cambridge: Cambridge University Press, 2022.  </p>
    <p> OpenAI. (2024). ChatGPT [Large language model]. https://chat.openai.com/chat. </p>
