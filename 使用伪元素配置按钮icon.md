![image](https://user-images.githubusercontent.com/20221918/165673176-28115fb1-ba8f-47b0-b603-bfd612143b40.png)

template
      
    <div class="card">
      <div class="card-body">
        <a href="" target="_blank" class="btn btn-docu" rel="noopener">Documentation</a>
      </div>
    </div>
          
style
      
    .card  .card-body .btn {
      display: block;
      width: 200px;
      height: 48px;
      line-height: 48px;
      background-color: blue;
      border-radius: 4px;
      text-align: center;
      color: #fff;
      font-weight: 700;
    }

    .card .card-body .btn-docu:before {
      content: "\0000a0";
      display: inline-flex;
      height: 24px;
      width: 24px;
      line-height: 24px;
      margin: 0px 10px 0px 0px;
      position: relative;
      top: 0px;
      left: 0px;
      background: url(https://stackdiary.com/docu.svg) no-repeat left center transparent;
      background-size: 100% 100%;
    }
