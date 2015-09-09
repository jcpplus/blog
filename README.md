# 1
 每次完成一章，都需要先清空数据库
 
# 2 
使用 `moment` 库，来调用时间，比起以下原生方法要来的简单明了。

    var time = {
        date: date,
        year: date.getFullYear(),
        month: date.getFullYear() + "-" + (date.getMonth() + 1),
        day: date.getFullYear() + "-" + (date.getMonth() + 1) + "-" + date.getDate(),
        minute: date.getFullYear() + "-" + (date.getMonth() + 1) + "-" + date.getDate() + " " +
            date.getHours() + ":" + (date.getMinutes() < 10 ? '0' + date.getMinutes() : date.getMinutes())
    }

[moment官方](http://momentjs.com/docs/#/displaying/)

    moment().format('MMMM Do YYYY, h:mm:ss a'); // 九月 9日 2015, 2:26:58 下午
    moment().format('dddd');                    // 星期三
    moment().format("MMM Do YY");               // 9月 9日 15
    moment().format('YYYY [escaped] YYYY');     // 2015 escaped 2015
    moment().format();                          // 2015-09-09T14:26:58+08:00
