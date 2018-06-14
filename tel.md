## 验证手机号的位数

    <style>
     span {
       color: red;
       display: none;
     }
     input {
         display: inline-block;
            margin-top: 20px;
            padding-bottom: 20px;
        }
     .yanz {
            background-color: red;
            color: aliceblue;
            width: 100px;
            text-align: center;
            line-height: 35px;
            margin-top: 20px;
        }
    </style>



    手机号:
    <br>
    <input type="text" placeholder="请输入手机号" class="iPhone">
    <span>格式不正确,请重新输入</span>
    <div>
        <input type="text">
        <div class="yanz">获取验证码</div>
    </div>


    <script>
        var span = document.querySelector('span')
        var iphone = document.querySelector('.iPhone')
        //正则表达式用来判断手机号的位数 及数字开头及结尾
        iphone.onblur = function () {
            // 判断第一位是否是1开头  第二位数字是3,4,5,6,7,8   里面是否包含0-9这些数字

            if (!/^1[34567]\d{9}$/.test(iphone.value)) {
                span.style.display = 'block'
            } else {
                // 打印输入的文本内容
                console.log(this.value)
                span.style.display = 'none'
            }
        }
    </script>
