# from
表单验证问题

if (eventObj.preventDefault) {
		   		eventObj.preventDefault();
			} else {
				window.event.returnValue = false;
			}
           	return false;
返回值很重要。当submit或click事件处理程序被调用并且返回false,浏览器就会停止提交过程。
如果不返回false，默认行为是继续并提交表单。在大多数浏览器中，可以通过调用preventDefault()方法中断默认行为。然而其在IE9以下的版本中不支持，所以先判断preventDefault()是否可用。否则将window.event对象的returnValue属性置为false
