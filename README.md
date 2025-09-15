# **Dashboard V3 Ecotron Server (ClickHouse)**

1. This project is a clone of the [Ecotron Dashboard V3 repository](https://bitbucket.org/ecofrostdevs/ecotron_dashboard_v3/src/main/) from Bitbucket. (APIs have been moved to ClickHouse)

   **`git clone https://bitbucket.org/ecofrostdevs/ecotron_dashboard_v3.git`**

2. This project is built using:
   - [Node.js](https://nodejs.org/) – JavaScript runtime
   - [Express.js](https://expressjs.com/) – Web framework for Node.js
   - [MongoDB](https://www.mongodb.com/) – NoSQL database for telemetry data
   - [ClickHouse](https://clickhouse.com/) – OLAP database for analytics & reporting
   - [MySQL](https://www.mysql.com/) – Relational database for metadata and configs

3. **`cd ecotron_dashboard_v3`**

4. Make sure you have Node.js (v18+) installed. Then run: **`npm install`**

5. Create Environment File
   Create a `.env` file in the root folder and add your configurations.

6. Start the Development Server - **`npm run dev`**

7. After starting the server, open [http://localhost:3033/api-docs/#/](http://localhost:3033/api-docs/#/) in your browser to view the Swagger API documentation and verify that the APIs are responding correctly. You can also use Postman to test the endpoints manually.
