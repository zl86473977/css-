我们使用 checkbox 输入类型，加上一个 :checked 伪类。当 :checked 返回 true 的情况时，我们使用 transform 属性更改状态。

你可以使用这种方法实现各种目标。比如，当用户点点击指定的复选框时候，切花到隐藏其内容。

在输入 input 类型的单选和复选框使用，当然，这也可以应用到`<option>`和`<select>`元素。

![image](https://user-images.githubusercontent.com/20221918/165668004-b9b7aeb8-f917-485d-9849-0163fd441781.png)


template
    
    <div class="checklist">
        <h2>Item Checklist with CSS</h2>
        <label>
            <input type="checkbox" name="" id="" />
            <i></i>
            <span>Item #1</span>
        </label>
        <label>
            <input type="checkbox" name="" id="" />
            <i></i>
            <span>Item #2</span>
        </label>
        <label>
          <input type="checkbox" name="" id="" />
          <i></i>
          <span>Item #3</span>
        </label>
    </div>
    
style
    
    .checklist {
        padding: 50px;
        position: relative;
        background: #043b3e;
        border-top: 50px solid #03a2f4;
    }
    .checklist h2 {
        color: #f3f3f3;
        font-size: 25px;
        padding: 10px 0;
        margin-left: 10px;
        display: inline-block;
        border-bottom: 4px solid #f3f3f3;
    }
    .checklist label {
        position: relative;
        display: block;
        margin: 40px 0;
        color: #fff;
        font-size: 24px;
        cursor: pointer;
    }
    .checklist input[type="checkbox"] {
        -webkit-appearance: none;
    }
    .checklist i {
        position: absolute;
        top: 2px;
        display: inline-block;
        width: 25px;
        height: 25px;
        border: 2px solid #fff;
    }
    .checklist input[type="checkbox"]:checked ~ i {
        top: 1px;
        height: 15px;
        width: 25px;
        border-top: none;
        border-right: none;
        transform: rotate(-45deg);
    }
    .checklist span {
        position: relative;
        left: 40px;
        transition: 0.5s;
    }
    .checklist span:before {
        content: '';
        position: absolute;
        top: 50%;
        left: 0;
        width: 100%;
        height: 1px;
        background: #fff;
        transform: translateY(-50%) scaleX(0);
        transform-origin: left;
        transition: transform 0.5s;
    }
    .checklist input[type="checkbox"]:checked ~ span:before {
        transform: translateY(-50%) scaleX(1);
        transform-origin: right;
        transition: transform 0.5s;
    }
    .checklist input[type="checkbox"]:checked ~ span {
        color: #154e6b;
    }
    
