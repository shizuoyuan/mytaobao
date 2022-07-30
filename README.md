# mytaobao![charector](https://user-images.githubusercontent.com/69787782/181866847-2b38a368-789a-4806-aed6-429d5fe7c8fc.png)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
<script>

/*

小花是个聪明的孩子，对数学特别感兴趣，

他偶然得到两个正整数a和b，现在他拿任何一个数 x 作如下运算，

y=（div（x，b）/mod(x，b)）。

其中div是整除运算，mod是取余运算，/是正常除法运算，


小华认为，如果一个正整数x使得y也是一个正整数,
且在区间【1，a】内，就说x是一个"好数"。

现在请你计算，所有好数的 和是多少，由于答案过大，

请输出答案模除1000000007后的值。，，，，，，，，

输入两个整数a.b (1<=a，b<=10000000)，，，，，，，，

输入2，2 
计算结果是 8

*/

function div(num1,num2){
   return parseInt(num1/num2)
}

// 求一个数是不是好数
function isHao(x,a,b){
    if(x%b==0){
        return false;
    }
    let y = (div(x,b)/(x%b));
    let zheng = false;
    if(y==0){                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 
        zheng = false;
    }else if(parseInt(y)==y){
        //y是正整数
        zheng =  true;
    }else{
        zheng = false;
    }

    if(zheng && (y>=1 && y<=a)){
        return true
    }
    return false;
}
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             
function sumHao(a,b){
    let sum = 0;
    for(let x = 1;x<1000000;x++){
        if(isHao(x,a,b)){
            sum += x;
        }
    }
    return sum%1000000007;
}

console.log(sumHao(2,2));


</script>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
