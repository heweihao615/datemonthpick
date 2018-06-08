# datemonthpick
年月控件，选择年月、之后的年月不可选~
## 使用：
### 1.引入依赖
### 2.js使用：
`$("someinput").DatePicker();`
#### 初始化时间:

let Initdatetime = (el) => {

            moment.lang('zh-cn', {
            
                week: {
                
                    dow: 1 // Monday is the first day of the week
                    
                }
                
            });
            
            var date = new Date(), y = date.getFullYear(), m = date.getMonth();
            
            var _nowDay = new Date(y, m);
            
            _nowDay = moment(_nowDay).format("YYYY-MM");
            
            $(el).val(_nowDay);
            
        }
        
//获取当前月的最后一天，加上０１可选择某月开始和结束年月

                function getCurrentMonthLast(year, month) {
                
                    //year + '-' + month + '-' + new Date(year, month, 0).getDate();
                    
                    return  new Date(year, month).toJSON().substring(0, 10);
                    
                }
