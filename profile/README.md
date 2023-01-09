# Welcome to BiteMe 🐍

BiteMe is an online multiplayer snake game played on a shared screen. Enjoy some competitive fun with your friends by playing this all-time classic! 
Simply scan the QR code and control the snake on the screen using your phone.

## Two Frontends - gamescreen and controller
Tech stack: <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="24px" title="react"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"  width="24px" title="Typescript" /> &nbsp; &nbsp; &nbsp; 
- The gamescreen frontend is where most of the game logic lies (growing and eating food, moving through the walls, dying and points counting) as well as rendering the snake movement, food display and all the other visual aspects.
- the controller has vibration feedback on touch (only on chrome)

## Backend as a service?
Tech stack: <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTRQV2FLjhIZLntvJwSJTeqL8u7Ao0rBn56XsYBACF080iHw7JwgTYxC4itT3YrO4qTopI&usqp=CAU" width="24px" title="AppSync"/> (AWS AppSync)
- The interesting part about this app is that it has no BE in the traditional sense, but leverages AWS AppSync, a fully managed GraphQL server to handle all the connections. Under the hood, it uses WebSocket technology, which gives the app a real-time feel. 
- Movement instructions were mutations sent from the controller through a subscription.

![architecture](https://user-images.githubusercontent.com/63497846/211324001-08dc85f4-4637-45da-a397-0fb662c5a682.png)

## DevOps and Infrastructure
Tech stack: <img src="https://archive.org/download/github.com-actions-starter-workflows_-_2020-01-25_22-21-15/cover.jpg" width="24px" title="Github Actions" /> &nbsp; | &nbsp; <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" width="24px" height="24px" title="aws"/> 
- the whole app is deployed on AWS, the two FE deployed on S3 and distributed through CloudFront
