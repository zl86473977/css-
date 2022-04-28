核心代码 ： content: attr(tooltip-data)，让content只想标签的自定义属性tootip-data

![image](https://user-images.githubusercontent.com/20221918/165666709-8af8ec0c-d189-429c-aed4-357fc0da322b.png)


template

    <h1>
      HTML/CSS tooltip
    </h1>
    <p>
      Hover <span class="tooltip" tooltip-data="Tooltip Content">Here</span> to see the tooltip.
    </p>
    <p>
      You can also hover <span class="tooltip" tooltip-data="This is another Tooltip Content">here</span> to see another example.
    </p>

style
    
    .tooltip {
      position: relative;
      border-bottom: 1px dotted black;
    }

    .tooltip:before {
      content: attr(tooltip-data); 
      position: absolute;
      width: 250px;
      background-color: #efba93;
      color: #fff;
      text-align: center;
      padding: 15px;
      line-height: 1.1;
      border-radius: 5px;
      z-index: 1;
      opacity: 0;
      transition: opacity .5s;
      bottom: 125%;
      left: 50%;
      margin-left: -60px;
      font-size: 0.70em;
      visibility: hidden;
    }

    .tooltip:after {
      content: "";
      position: absolute;
      bottom: 75%;
      left: 50%;
      margin-left: -5px;
      border-width: 5px;
      border-style: solid;
      opacity: 0;
      transition: opacity .5s;
      border-color: #000 transparent transparent transparent;
      visibility: hidden;
    }

    .tooltip:hover:before, 
    .tooltip:hover:after {
      opacity: 1;
      visibility: visible;
    }
