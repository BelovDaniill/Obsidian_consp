
**main всегда publick static void**

**Garbage collector** - под процесс работающий параллельно с основным кодом и удаляющий все динамические переменные после последнего использования => если объект используется только 1 раз - его лучше создать без имени.

Можно создавать безымянные объекты: 
```java 
new Class().fun();
```

Любое дробное число по умолчанию **double** , любое целое **int**

Создание переменной определённого типа: 
```java
floatvar = 0.99f / (float)0.99 
```

Вывод: 
```java
void fun()  
{System.out.println("sth" + var)}
```

Пример программы:

```java
class Studnet {
	String name;    // 
	Float lazynass; // коэффициент лени от 0-1 где 1 это ленивый
	Byte IQ;        // (максимальное значение 127) 80-127 
	int exams;      // кол-во экзаменов
	int marks[]     // кол-во оценок
	
	Studnet () {    // конструктор класса студент
		name = "Pantera";
		lazynass = (FLoat)0.67; // 0.67f
		IQ = (Byte)127;
		exams = 6;
		marks = new int[exams];
		for(int i = 0; i < exams; i++) {
			marks[i] = 7;
		}
	}
	
	Student (Float lazynass, Byte iq) { // конструктор с параметром
		name = "Erick";
		this.lazynass = lazynass; // чтобы небыло конфликта надо использовать this
		IQ = iq; // конфликта имён не будет так как разные регистры
		exams = 18;
		marks = new int[exams];
		for(int i = 0; i < exams; i++) {
			marks[i] = 8;
		}
	}
	
	Studnet (Studnet other) {    // конструктор копирования
		name = other.name;
		lazynass = other.lazynass;
		IQ = other.IQ;
		exams = other.exams;
		marks = new int[exams];
		for(int i = 0; i < exams; i++) {
			marks[i] = other.marks[i];
		}
	}
	
	void echo() {
		System.out.println("name: " + this.name);
		System.out.println("lazynass: " + this.lazynass);
		System.out.println("IQ: " + this.IQ);
		System.out.println("exams: " + this.exams);
		// вывод массива
		for (int i; i < exams; i++) {
			System.out.print(" " + this.exams[i]);
		}
	}
}
```