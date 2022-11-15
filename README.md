
<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
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




<!-- PROJECT LOGO -->
<br />
<div align="center">
  <p align="center">
  <img src="PATH PLANNING PROJECT AAE 2004 GROUP 07.png" alt="animated" width="600" height="350"/>
</p>
  <h2 align="center">AAE 2004 Group 7 Project</h3>

  <p align="center">
    =========
    <br />
    <br />
    <br />
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#background-of-path-planning-to-aviation-engineering">Background of Path Planning to Aviation Engineering</a>
    </li>
    <li>
      <a href="#theory-of-path-planning-algorithm">Theory of Path Planning Algorithm</a>
    </li>
    <li>
      <a href="#introduction-of-the-engineering-tools">Introduction of the Enginnering Tools</a>
      <ol type = "a">
        <li><a href="#python">Python</a></li>
        <li><a href="#github">Github</a></li>
      </ol>
    </li>
    <li>
      <a href="#task-1-methodology-results-and-discussion">Task 1: Methodology, Results and Discussion</a> 
       <ol type="a">
         <li><a href="#methodology">Methodology</a></li>
         <li><a href="#results">Results</a></li>
         <li><a href="#discussion">Discussion</a></li>
        </ol>
       </li>
     <li>
      <a href="#task-21-methodology-results-and-discussion">Task 2.1: Methodology, Results and Discussion</a> 
       <ol type="a">
         <li><a href="#methodology">Methodology</a></li>
         <li><a href="#results">Results</a></li>
         <li><a href="#discussion">Discussion</a></li>
        </ol>
       </li>
    <li>
     <a href="#task-22-methodology-results-and-discussion">Task 2.2: Methodology, Results and Discussion</a> 
       <ol type="a">
         <li><a href="#methodology">Methodology</a></li>
         <li><a href="#results">Results</a></li>
         <li><a href="#discussion">Discussion</a></li>
        </ol>
       </li>
    <li>
     <a href="#task-3-methodology-results-and-discussion">Task 3: Methodology, Results and Discussion</a> 
       <ol type="a">
         <li><a href="#methodology">Methodology</a></li>
         <li><a href="#results">Results</a></li>
         <li><a href="#discussion">Discussion</a></li>
        </ol>
       </li>
    <li>
      <a href="">Reflective Essay</a>
       <ol type = "a">
         <li><a href="#sahat-mahmud">Sahat Mahmud</a>
         <li><a href="#muhammad-inamul-haq">Muhammad Inamul Haq</a>
         <li><a href="#yajiao-liu">Yajiao Liu</a>
         <li><a href="#ma-fandhu">Ma Fandhu</a>
         <li><a href="#miao-kaili">Miao Kaili</a>
         <li><a href="#ziyang-liu">Ziyang Liu</a>
         <li><a href="#abcd">abcd</a>
       </ol>
      <li>
         <a href="#references">References<a>
       </li>
  </ol>
</details>



<!-- BACKGROUND OF PATH PLANNING TO AVIATION ENGINNERING -->
## Background of Path Planning to Aviation Engineering

=============

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- THEORY OF PATH PLANNING ALGORITHM -->
## Theory of Path Planning Algorithm

 For path planning, we used the A* algorithm, which combines the advantages and disadvantages of the depth-first search algorithm and the breadth-first search algorithm. It constructs a cost function based on a heuristic function that takes into account both the cost of the distance of the new node from the initial point and the cost of the distance of the new node from the target point. A* algorithm requires the maintenance of two state tables, non-separately called the openList and the closeList . OpenList consists of nodes to be examined, and CloseList consists of nodes that have already been examined.

The specific process： Firstly, we need to simplify the search area. Assuming that there is a barrier between the Start node and the Target node, and then, we rasterize the map and name the center of each square as a node, which reduces our search area to a 2-dimensional array. Each item of the array represents a grid, and its state is walkable and unwalkable. The path is found by working out which squares need to be walked through to get from the Start node to the Target node
 
Then we start searching to find the shortest path. In the beginning, we add the starting point to the openList. And from the starting point, check its neighboring squares and then expand in all directions until the goal is found. Afterward, we select the node with the lowest cost of movement among the nodes adjacent to the Start node and move it to the closeList based on the movement cost evaluation function f(n)=g(n)+h(n) (f(n) is the estimated cost of moving from the initial state to the target state via state n, g(n) is the actual cost of moving from the initial state to state n in the state space, and h(n) is the estimated cost of the best path from state n to the target state). 

For the 8 adjacent squares of the current square.
a: if it is unreachable or it is in the closeList, ignore it.
b: if it is not in the openList, add it to the openList and set the current square as its parent, recording the f, g , and h values for that square.
c: if it is already in the openList, check if this is a better path, using the g value as a reference; a smaller g value means this is a better path. If the g value is smaller, set the parent of that node to the current square and recalculate its g and h values.

Repeat the above process until the target node is searched, completing the path search and ending the algorithm



<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- INTRODUCTION OF THE ENGINEERING TOOLS -->
## Introduction of the Engineering Tools

=======
### Python


### Github


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- TASK 1: METHODOLOGY, RESULTS AND DISCUSSION -->
## Task 1: Methodology, Results and Discussion


### Methodology

### Results

### Discussion


<!-- TASK 2: METHODOLOGY, RESULTS AND DISCUSSION -->
## Task 2: Design a new cost area that can reduce the cost of the route


In the progress of solving Task 2, we know that the area of the cost reduction area is fixed according to the given conditions. So if we want to minimize the final navigation cost, the goal we need to achieve is to make the shipping route through the selected area as long as possible. In choosing this cost reduction area, our initial idea is to first set up a block with constant horizontal coordinates and shifting vertical coordinates. Then the vertical coordinates of the region are made to move from the lowest to the highest point at a unit rate of one frame at a time, and the length of the route through the selected region in Task 1 is calculated. At the same time, these length data and the corresponding index of the longitudinal coordinates are stored in a list. When the cycle is completed, the largest data in the list and its corresponding vertical coordinates are found. At this point, we can get the location of the best region. However, since it was not possible to define the lengths of the regions through which the routes in Task 1 passed, we were not able to compare the lengths through which the routes passed in all the location regions according to the initial idea. In order not to interfere with the project, we had to fuzzify the selection of regions in order to find a value approximately close to the correct result.The specific code is shown in the figure below.
  ![image](https://user-images.githubusercontent.com/116137460/201840004-8ade6802-be42-4ea3-96bf-8aaea1134e5a.png)
  And the result of the code is just like the plot:
  
  <img width="561" alt="image" src="https://user-images.githubusercontent.com/116137460/201842870-9db4b330-32f0-4e58-b991-2c5266585cd6.png">






<!-- TASK 3: METHODOLOGY, RESULTS AND DISCUSSION -->
## Task 3: Design a new aircraft model within the constrains to achieve minimum cost for your group challenge
For task3, we need to come up with a suitable aircraft based on the given conditions, such as the number of passengers, fuel bills, fixed costs, etc. At the very beginning, we think it is like a maths problem and our idea to solve this task is divided into two situations, one is when the passenger capacity of the aircraft is less than 300, and the other is when the passenger capacity of the aircraft is more than 300. We can write an equation in code based on given conditions to know the lowest cost and the most suitable aircraft capacity. But when we tried to do this, we found that the number of passengers we calculated was not an integer. After we thought about it for a while, we realized that when we were programming, we didn't define the unknowns enough, which led to inaccurate results. After modifying the code, the program ran correctly and came to a conclusion.
  ![752e8669f0e086ac9c495ed64db5cfe](https://user-images.githubusercontent.com/116135818/201843643-adcf8a6f-50ca-489c-8d97-ad163bdb0699.jpg)

  ![d7e117580bc20c0bebfa34588fbdb17](https://user-images.githubusercontent.com/116135818/201835915-d3538100-da8c-40a2-9f61-857d1d828d9a.png)
  
<img width="973" alt="807c72a9b943e31fb2b3e66bf9b1b2d" src="https://user-images.githubusercontent.com/116135818/201843862-d5427733-a0e5-4fe2-bef1-c653c1cb9084.png">

Like the picture1 and picture 2 showed, we defined all the condition  and list equation. Then we can find the minimum cost in the list through code. What's more, we add a code "PC%50==0" to make the final answer is a integer. And the third picture showed our final result. 


<!-- REFLECTIVE ESSAY -->
## Reflective Essay

### Sahat Mahmud

### Muhammad Inamul Haq

### Yajiao Liu

### Miao Kaili

### Ziyang Liu
  The group project was successfully completed with the efforts of our team members. In working on this project, I was mainly responsible for the code research and reporting for Task 2. During the initial solution of Task 2, I was inspired by the principle of copying machine and wanted to make a defined line to scan from bottom to top for different positions of calculation. However, due to my limited ability to write code, I asked the rest of the group for help. The other members were quick to discuss this with me and put a lot of effort into solving the puzzle. However, the progress of the project was slowed down by the time spent on the code for Task 2. For the sake of the project and the rest of the group, I chose a less rigorous but achievable approach with the agreement of the other members. Although I did not perform as well as expected in this group task, I still acquired a lot of thinking and knowledge about writing code. At the same time, I felt the amazing efficiency and better solutions that come from working together with the group members, and I grew to enjoy the feeling of getting immediate feedback on the ideas I proposed. All in all, this AAE group project has benefited me a lot both in terms of professional knowledge and cooperative interaction.

### Ma Fanshu

### abcd


<!-- References -->
https://blog.csdn.net/weixin_42301220/article/details/125140910

============
============

<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
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
