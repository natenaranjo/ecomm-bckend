<div id="top"></div>
<!--
*** Thanks for checking out the retail-backend. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h2 align="center">Retail Backend</h2>

  <p align="center">
    <br />
    <a href="https://github.com/natenaranjo/retail-backend"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://watch.screencastify.com/v/IHHGCqZ8zDG8euFlOagM">View Demo</a>
    ·
    <a href="https://github.com/natenaranjo/retail-backend/issues">Report Bug</a>
    ·
    <a href="https://github.com/natenaranjo/retail-backend/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

This assignment was to build a ecommerence backend that allow the user to create, update, and delete product, tag, and category if need be using sequelize.  

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

This assignment used the following to be built with:

- Node
- Sequelize
- Mysql2
- Dotenv

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get started clone the repo to your drive, then follow the steps below.

### Prerequisites
Only need npm to get started.
* npm
  ```sh
  npm install
  npm run start
  ```

### Installation

_Follow the steps below:_

1. Clone the repo
   ```sh
   git clone https://github.com/natenaranjo/retail-backend.git
   ```
2. Install NPM packages
   ```sh
   npm install
   ```
3. Create the Database
    ```
    mysql -u root -p

    SOURCE db/schema.sql

    exit
4. Seeding the Database
   ```sh
   node ./seeds/index.js
   ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

1. Start the app
    ```
    npm run start
    ```
2. Open Insomina
    ```
    localhost:3001
    ```
3. Insomnaa use GET method on Products, Tags, Categories
    ```
    localhost:3001/api/products

    localhost:3001/api/tags

    localhost:3001/api/categories
    ```
4. Insomnaa use POST method on Products, Tags, Categories to create a new one
   - Products
        ```
        localhost:3001/api/products
        ```
        Add the following in the json editor in Insomnia, then press send.  
        ``` json
        {
            "product_name": "Star Wars: Battlefront",
            "price": "49.99",
            "stock": "200",
            "category_id": [6],
            "tagIds": [9, 10, 11]
        }
        ```
        If you use the GET method again on products then you will see it added at the bottom.
    - TAGS:
        ```
        localhost:3001/api/tags
        ```
        Add the following in the json editor in Insomnia, then press send
        ``` json
            {
                "tag_name": "Action"
            }
        ```
        If you use the GET method again on tags then you will see it added at the bottom.
    - Categories:
        ```
        localhost:3001/api/categories

        ```
        Add the following in the json editor in Insomnia, then press send
        ``` json
            {
                "category_name": "Star Wars"
            }
        ```
        If you use the GET method again on tags then you will see it added at the bottom.
        
5. Insomnia use PUT method on any Products, Tags, Categories the id:
    - Products
        Need to put the id of item you want to update behind /products/
        ```
        localhost:3001/api/products/:ID
        ```
        Update the product information you want to update, then press send. 
        ``` json
        {
            "product_name": "Star Wars: Battlefront",
            "price": "49.99",
            "stock": "200",
            "category_id": [6],
            "tagIds": [9, 10, 11]
        }
        ```
        If you use the GET method again on products then you will see it added at the bottom.
    - TAGS:
        Need to put the id of item you want to update behind /tags/
        ```
        localhost:3001/api/tags/:ID
        ```
        Update the tag name, then press send to update.
        ``` json
            {
                "tag_name": "Action"
            }
        ```
        If you use the GET method again on tags then you will see it added at the bottom.
    - Categories:
        Need to put the id of item you want to update behind /categories/
        ```
        localhost:3001/api/categories/:ID

        ```
        Update the category name, then press send.
        ``` json
            {
                "category_name": "Star Wars"
            }
        ```
        If you use the GET method again on tags then you will see it added at the bottom.
6. Insomnia use DELETE method on any Products, Tags, Categories by the id:
    ```
    localhost:3001/api/products/{id number here}

    localhost:3001/api/tags/{id number here}

    localhost:3001/api/categories/{id number here}
    ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ROADMAP -->
## Roadmap

- [x] Building the ENV FILE
    - [x] Add Database Name
    - [x] Add Mysql User
    - [x] Add Mysql Password
- [x] Connect Database to Sequelize
- [x] Build Schema and Seed File
- [x] When the Server is started the Sequelize models are synced to Mysql Database
- [x] Insomina using the GET Route pull data from database:
    - [x] GET /api/products
    - [x] GET /api/tags
    - [x] GET /api/categories
- [x] Insomina using the Update Route to update by ids:
    - [x] PUT /api/products/:id
    - [x] PUT /api/tags/:id
    - [x] PUT /api/categories/:id
- [x] Incomina using the Delete Route to remove by ids:
    - [x] DELETE /api/products/:id
    - [x] DELETE /api/tags/:id
    - [x] DELETE /api/categories/:id



<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@rezzingonweb3](https://twitter.com/rezzingonweb3) - natenaranjodev@gmail.com


<p align="right">(<a href="#top">back to top</a>)</p>





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/natenaranjo/retail-backend.svg?style=for-the-badge
[contributors-url]: https://github.com/natenaranjo/retail-backend/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/natenaranjo/retail-backend.svg?style=for-the-badge
[forks-url]: https://github.com/natenaranjo/retail-backend/network/members
[stars-shield]: https://img.shields.io/github/stars/natenaranjo/retail-backend.svg?style=for-the-badge
[stars-url]: https://github.com/natenaranjo/retail-backend/stargazers
[issues-shield]: https://img.shields.io/github/issues/natenaranjo/retail-backend.svg?style=for-the-badge
[issues-url]: https://github.com/natenaranjo/retail-backend/issues
[license-shield]: https://img.shields.io/github/license/natenaranjo/retail-backend.svg?style=for-the-badge
[license-url]: https://github.com/natenaranjo/retail-backend/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/natenaranjo
[product-screenshot]: screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 