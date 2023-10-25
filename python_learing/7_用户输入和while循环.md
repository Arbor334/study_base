## 用户输入

### 用户输入input()方法

> 工作原理: input()函数让程序暂停运行，等待用户输入一些文本，获取用户输入后，python将其赋给一个变量，以方便程序员使用。

> ```python
> message=input("please input a number and l will tell you back:")
> print(message)
> ```

> 输入的信息赋给message变量
> 
> 注意 :disappointed_relieved:input()赋给message的是字符串变量

### int()获取数值输入

> ```python
> age=input("how old are you ：")
> age=int(age)
> 
> if age < 18:
>     print("你还没有成年")
> else:
>     print("恭喜你，成年了") 
> ```

> int()函数将数的字符串表示转换为数值表示

### 求模运算

> ```python
> number=input("请输入一个数字:")
> number=int(number)
> if number %2 ==0:
>     print("你输入的是偶数")
> else:
>     print("你输入的是奇数")
> ```

## while 循环

> ```python
> current_number=1
> while current_number < 5 :
>     print(f"{current_number}")
>     current_number+=1
> ```

### 让用户选择何时停止

> ```python
> prompt="tell me something,and I will repeat it back to you"
> prompt+="\nEnter 'quit' to end the program:"
> message ="" # 提前设定一个空字符串，让message有东西可以与quit比较
> while message !='quit':
>     message=input(prompt)
>     if message != 'quit':
>         print(message)
> ```

### 使用标志

> ```python
> prompt="tell me something,and I will repeat it back to you"
> prompt+="\nEnter 'quit' to end the program:"
> active=True
> while active:
>     message=input(prompt)
>     if message == 'quit':
>         active=False
>     else:
>         print(message)
> ```

### 使用break 退出循环

> ```python
> prompt="tell me something,and I will repeat it back to you"
> prompt+="\nEnter 'quit' to end the program:"
> 
> while True:
>     message=input(prompt)
>     if message == 'quit':
>         break
>     else:
>         print(message)
> ```

### 在循环中使用continue

> ```python
> current_number=0
> while current_number < 10:
>     current_number += 1
>     if current_number %2 == 0:
>         continue
>     print(current_number)
> 
> ```

### 使用while循环处理列表和字典

> 在遍历列表的同时对其进行修改，可使用while循环
> 
> ```python
> unconfirmed_users=['alice','brian','candace']
> confirmed_users=[]
> while unconfirmed_users:
>     current_user=unconfirmed_users.pop() # pop()方法
>     print(f"Verifying user: {current_user.title()}")
>     confirmed_users.append(current_user)
> 
> print("\n The following users have been confirmed:")
> for confirmed_user in confirmed_users:
>     print(confirmed_user.title())
> ```

### 删除为特定值的所有列表元素 remove()方法

> ```python
> pets=['dog','cat','dog','goldfish','cat','rabbit','cat']
> print(pets)
> 
> while 'cat' in pets:
>     pets.remove('cat')
> 
> print(pets)
> ```

### 用户输入填充字典

> ```python
> responses={}
> 
> polling_active=True
> 
> while polling_active:
>     name=input("\n what is your name？")
>     response=input("Which mountain would you like to climb someday?")
>     responses[name]=response
>     repeat=input("would you like to let  another person respond?(yes/no)")
>     if repeat=='no':
>         polling_active=False
> 
> print("\n--- Poll Results ---")
> for name, response in responses.items():
>     print(f"{name} would like to climb {response}.")
> ```


