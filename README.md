to do list
========================
Програма “to do list” – предназначена для создания списка задач. Програма помогает управлять списками дел, реализовать запланированые задачи и ничего не забыть. Пользователь имеет возможность создавать список задач, в процессе их выполнения, может изменять удалять, завершать.Програма реализована на языке программирования javascript (ES6) c использованием React.js

Описание интерфейса
========================
![image](https://user-images.githubusercontent.com/65450885/145360143-23131eb9-2ee5-4bb0-bdd1-550cc9561d7c.png)

При вводе задач,функция AddTask добавляет задачу в список.
```  
const addTask = (userInput) => {
    if(userInput) {
      const newItem = {
        id: Math.random().toString(36).substr(2,9),
        task: userInput,
        complete: false
      }
      setTodos([...todos, newItem])
    }
  }
```
![image](https://user-images.githubusercontent.com/65450885/145360828-e0876023-82f6-4fe1-bb90-f51816391b0c.png)

Возможность добавления в список осуществляется по нажатию клавиши enter, реализованно с помощью функции handleKeyPress:
```  
  const handleKeyPress = (e) => {
        if(e.key === "Enter") {
            handleSubmit(e)
        }
    }
```
Удаление из списка происходит по нажатию на "X", реализованно с помощью функции:
```  
  const removeTask = (id) => {
    setTodos([...todos.filter((todo) => todo.id !== id)])
  }
```
