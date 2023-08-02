## ⭐️객체지향 프로그램이란?

객체지향 프로그램(Object-Oriented Programming, OOP)이란 컴퓨터 프로그램을 어떤 데이터를 입력받아 순서대로 처리하고 결과를 도출하는 명령어들의 목록으로 보는 시각에서 벗어나 여러 독립적인 부품들의 조합, 즉 객체들의 유기적인 협력과 결합으로 파악하고자 하는 컴퓨터 프로그래밍의 패러다임을 의미한다.
자동차를 만든다고 할 때, 수 많은 부품들의 결합과 연결로 하나의 완전한 자동차가 만들어지는 것과 같다고 할 수 있다. 객체지향적으로 소프트웨어를 설계한다는 말의 의미는 어떤 프로그램의 일부분에 해당하는 작은 부품, 즉 객체를 먼저 만들고 이렇게 만들어진 여러 객체들을 조립해서 하나의 완성된 프로그램을 만드는 프로그래밍 방법론을 뜻한다.

## ⭐️객체지향 프로그램의 장점

- 객체 지향적 설계를 통해서 프로그램을 보다 유연하고 변경이 용이하게 만들 수 있다는 점이다. 마치 컴퓨터 부품을 갈아 끼울 대, 해당하는 부품만 쉽게 교체하고 나머지 부품들을 건드리지 않아도 되는 것처럼 소프트웨어를 설계할 때 객체 지향적 원리를 잘 적용해 둔 프로그램은 각각의 부품들이 각자의 독립적인 역할을 가지기 때문에 코드의 변경을 최소화하고 유지보수를 하는데 유리하다.
- 코드의 재사용을 통해 반복적인 코드를 최소화하고, 코드를 최대한 간결하게 표현할 수 있다. 또한 객체 지향 프로그래밍은 실제 우리가 보고 경험하는 세계를 최대한 프로그램 설계에 반영하기 위한 지속적인 노력을 통해 발전해왔기 때문에, 보다 인간 친화적이고 직관적인 코드를 작성하기에 용이하다.
- 객체 지향 프로그래밍의 4가지 특징은 추상화, 상속, 다형성, 캡슐화인데, 모두 이러한 객체 지향적 설계의 이점들을 가장 잘 살릴 수 있는 방향으로 발전되어 왔다고 할 수 있다.

## ⭐️객체(Object)란?

객체는 객체지향 프로그랭의 가장 기본적인 단위이자 시작점이라고 할 수 있다. 객체지향 개념의 가장 기본적인 전제는 실제 세계는 객체들로 구성되어 있으며, 보여지는 모든 현상와 발생하는 모든 사건의 이러한 객체들 간의 상호작용을 통해 발생한다는 것에서 출발한다.
객체지향 프로그래밍에서는 이와 같은 각각의 객체를 추상화시켜 속성(state)과 기능(behavior)으로 분류한 후에 이것을 다시 각각 변수(variable)와 함수(function)로 정의하고 있다.

## ⭐️객체지향 프로그래밍의 4가지 특징

객체지향 프로그래밍이 우리가 보고 인지하는 실제 세계를 흉내 내어 가장 기본적인 단위인 객체들을 만들고, 그것들 간의 유기적인 상호작용을 규정하여 프로그램을 발전시키는 프로그래밍 방법론임을 이해할 수 있었다.
또한, 객체 지향적 설계를 통해 소프트웨어를 개발하면 코드의 재사용을 통해 반복적인 코드를 최소화하고, 보다 유연하고 변경이 용이한 프로그램을 만들 수 있다는 사실을 알게 되었다.

### 1. 추상화

추상이라는 용어의 사전적 의미를 보면 "사물이나 표상을 어떤 성질, 공통성, 본질에 착안하여 그것을 추출하여 파악하는 것"이라 정의하고 있다. 여기서 핵심이 되는 개념은 "공통성과 본질을 모아 추출"한다는 것이다.

예를 들면, 서울의 지하철 노선도는 서울의 지리를 추상화시켜서 보여주는 대표적인 예라고 할 수 있다. 중요한 부분을 강조하기 위해 불필요한 세부 사항들은 제거하고 가장 본질적이고 공통적인 부분만을 표출하여 표현하는 것과 관련 있다.

![스크린샷 2023-07-31 오후 1 50 13](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/fa5364da-ff21-4ef8-8844-d7aa68c4419d)
위에 예시를 보면, 자동차와 오토바이는 모두 이동수단이며 모든 이동 수단은 전진과 후진을 할 수 있다는 공통점을 가진다. 이것을 자바 문법 요소를 사용하여 표현하면, 자동차와 오토바이라는 하위 클래스(sub-class)들의 공통적인 기능(전진과 후진)을 추출하여 이동 수단이라는 상위 클래스(super class)에 정의 했다. 위에 예제에서는 편의상 공통적인 기능(메서드)만 추출했지만, 공통적인 속성(변수)도 추출하여 선언하는 것이 가능하다.

위에서 본 내용을 코드로 표현해보면 다음과 같다. 자바에서 추상화를 구현할 수 있는 문법 요소로는 추상클래스(abstract class)와 인터페이스(interface)가 있는데 아래 예제는 인터페이스를 사용한 예제이다.

```
public interface Vehicle {
   public abstract viod start()
   void moveForward();   //public abstract 키워드 생략 가능
   void moveBackward();
}
```

가장 먼저 자동차와 오토바이의 공통적인 기능 출루하여 이동 수단 인터페이스를 정의한다. 컴퓨터 프로그래밍에서 인터페이스란 "서로 다른 두 시스템, 장치, 소프트웨어 따위를 서로 이어주는 부분 또는 그런 접속 장치"이라 정의할 수 있는데, 객체 지향적 설계에 있어서 인터페이스는 어떤 객체의 역할만을 정의하여 객체들 간의 관계를 보다 유연하게 연결하는 역할을 담당한다.

다른 말로 표현하면, 인터페이스에는 추상 메서드나 상수를 통해서 어떤 객체가 수행해야 하는 핵심적인 역할만을 규정해두고, 실제적인 구현은 해당 인터페이스를 구현하는 각각의 객체들에서 하도록 프로그램을 설계하는 것을 의미한다.

다른 말로 표현하면, 인터페이스에는 추상 메서드나 상수를 통해서 어떤 객체가 수행해야 하는 핵심적인 역할만을 규정해두고, 실제적인 구현은 해당 인터페이스를 구현하는 각각의 객체들에서 하도록 프로그램을 설계하는 것을 의미한다.

**Car Class**

```
public class Car implements Vehicle {
   @Override
   public void moveForward() {
              System.out.println("자동차가 앞으로 전진합니다. ");
   }

   @Override
   public void moveBackward() {
              System.out.println("자동차가 뒤로 후진합니다.");
   }
}
```

**MotorBike Class**

```
public class MotorBike implements Vehicle {
     @Override
     public void moveForward() {
              System.out.println("오토바이가 앞으로 전진합니다. ");
      }
     @Override
      public void moveBackward() {
               System.out.println("오토바이가 후진합니다.");
      }
}
```

위에서 확인할 수 있는 것처럼, Vfehicle 인터페이스를 구현한 구현체, Car와 MotorBike 클래스에서 앞서 우리가 인터페이스에 정의한 역할을 각각의 클래스의 맥락에 맞게 구현하고 있다. 즉, 각각 클래스 모두 전진과 후진의 기능을 공통적으로 가지지만, 차는 차의 시동을 걸어야 하고, 오토바이는 오토바이의 시동을 걸어야하기 때문에 그 구현은 각 클래스에 따라 달라야 할 것이다.

이것을 객체지향 프로그래밍에서는 역할과 구현의 분리라고 하며, 이 부분이 아래에서 살펴볼 다형성과 함께 유연하고 변경이 용이한 프로그램을 설계하는 데 가장 핵심적인 부분이라 할 수 있다. 객체지향 프로그래밍에서는 보다 유연하고 변경에 열려 있는 프로그램을 설계하기 위해 역할을 구현을 분리하는데, 여기서 역할에 해당하는 부분이 인터페이스를 통해 추상화될 수 있다.

### 2. 상속

상속이란 기존의 클래스를 재활용하여 새로운 클래스를 작성하는 자바의 문법 요소를 의미한다.
추상화의 연장선에서, 상속은 클래스 간 공유될 수 있는 속성과 기능들의 상위 클래스로 추상화 시켜 해당 클래스로부터 확장된 여러개의 하위 클래스들이 모두 상위 클래스의 속성과 기능들을 간편하게 사용할 수 있도록 한다.
즉, 클래스들 간 공유하는 속성과 기능들을 반복적으로 정의할 필요 없이 딱 한번만 정의해두고 간편하게 재사용할 수 있어 반복적인 코드를 최소화하고 공유하는 속성과 기능에 간편하게 접근하여 사용할 수 있도록 한다.
![스크린샷 2023-07-31 오후 2 34 16](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/b33e1104-1fb9-45de-aef5-a4e3422e10a3)
위에 그름을 보면 자동차와 오토바이가 있고, 각각의 기능과 속성들이 명시되어 있다. 이 중에서 빨간색으로 표시된 속성과 기능들은 자동차와 오토바이의 공통적인 부분들이고, 푸른색으로 표시된 부븐들은 그렇지 않는 부분들이다.

**Car Class**

```
public class Car {
    String model;
    String color;
    int wheels;

    boolean isConvertible; // Car 클래스 공유의 속성

    void moveForward() {
             System.out.println("앞으로 전진합니다.");
      }
    void moveBackward() {
             System.out.println("뒤로 후진합니다.");
      }
    void openWindow() { //Car클래스 고유의 기능
             System.out.println("모든 창문을 엽니다.");
      }
}
```

**MotorBike Class**

```
public class MotorBike {
     String model;
     String color;
     int wheels;

     boolean isRaceable;

     void moveForward() {
              System.out.println("앞으로 전진합니다.")
      }
     void moveBackward() {
              System.out.println("뒤로 후진합니다.")
      }
     public void stunt()) { //클래스 고유의 기능
              System.out.println("Bike가 묘기를 부립니다.")
      }
}
```

위에 코드 예제를 보면, 한 눈에도 같은 코드가 반복적으로 정의되고 있다는 사실을 알 수 있다. 좀 더 구체적으로 보면, 각각의 클래스마다 속성으로 model, color, wheels 기능으로 moveForward()와 moveBackward가 완전히 동일한 코드임에도 불구하고 계속 반복되고 있다는 점을 확인할 수 있다. 또한 하나의 코드에서 변경사항이 일어나면, 해당 코드의 변경사항을 다른 클래스에서도 일일이 수정해하는 어려움이 있다.

이제 추상화와 상속을 활용하여 앞선 코드를 재정의를 해보도록 하겠다.

![스크린샷 2023-07-31 오후 3 07 52](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/ea4888f8-2820-4943-9273-639f79007113)
**Vehicle Class**

```
public class vehicle {
     String model;
     String color;
     int wheels;

    void moveForward() {
             System.out.println("전진합니다.");
     }
    void moveBackward() {
             System.out.println("후진합니다.");
     }
}
```

**Car Class**

```
public class Car extends Vehicle {
       boolean isConvertible;

      void openWindow () {
             System.out.println("모든 창문을 엽니다.");
      }
}
```

**MotorBike Class**

```
public class MotorBike extends Vehicle {
      boolean isRaceable;

     @Override
      void moveForward() {
               System.out.prinln("오토바이가 앞으로 전진합니다.");
      }
      public void stunt() {
               System.out.println("오토바이로 묘기를 부립니다,");
      }
}
```

**Main Class**

```
public class Main {
       public static void main(String[] args) {
                // 객체 생성
                Car car = new Car();
                MotorBike motorBike = new MotorBike();

               //car 객체의 속성 정의
                car.model = "테슬라";
                car.color = "빨강색";

                System.out.println("나의 자동차는" + car.color + " " + car.model + "입니다." );

               //car 객체의 기능 실행
                car.moveForward();
                motorBike.moveForward();
                motorBike.moveBackward();
       }
}

//출력값
나의 자동차는 빨강색 테슬라 입니다.
전진합니다.
오토바이가 앞으로 전진합니다.
후진합니다.
```

위에 코드 예제를 보면, Car와 MotorBike클래스의 공통적인 속성과 기능들을 추출(추상화)하여 Vehicle클래스 (상위 클래스)에 정의하였거, extends 키워드를 통해 각각의 하위 클래스로 확장하여 해당 기능과 속성들을 매번 반복적으로 정의해야 하는 번거로움을 제거했다. 또한, 공통적인 코드의 변경이 있는 경우 상위 클래스에서 단 한번의 수정으로 모든 클래스에 변경 사항이 반영될 수 있도록 만들었다.
참고로, MotorBike클래스에서 확인할 수 있듯이, 상위 클래스의 기능과 속성들을 그대로 사용할 수도 있지만, 각각의 클래스의 맥락에 맞게 메서드 오버라이딩(method overriding)을 사용하여 내용을 재정의할 수도 있다.

이부분이 추상화에서 봤었던 인터페이스를 통한 구현과 상속을 구분하는 핵심적인 차이 중에 하나라고 할 수 있다. 즉, 양자 모두 상위 클래스 항위클래스의 관계를 전제하면서 공통적인 속성과 기능을 공유할 수 있지만, 상속의 경우 상위 클래스의 속성과 기능들을 하위 클래스에서 그대로 받아 사용하거나 오바라이딩을 통해 선택적으로 재정의하여 사용할 수 있는 반면, 인터페이스를 통한 구현은 반드시 인터페이스에 정의된 추상 메서드의 내용이 하위 클래스에서 정의되어야 한다.

결론적으로, 상속 관계의 경우 인터페이스를 사용하는 구현에 비해 추상화의 정도가 낮다고 할 수 있다. 인퍼에시으가 역할에 해당하는 껍데기만을 정의해두었고, 하위 클래스에서 구체적인 구현을 하도록 강제하는 것에 비해, 상속 관계의 경우 상황에 따라 모든 구체적인 내용들을 정의해두고 하위 클래스에서는 그것을 단순히 가져다가 재사용할 수 있다.

### 3. 다형성

다형성이란 한자 이름 그대로 어떤 객체의 속성이나 기능이 상황에 따라 여러가지 형태를 가질 수 잇는 성질을 의미한다.
비유적으로 편하자면, 어떤 중년의 남성이 있다고 했을 때 그 남자의 역할이 아내에게는 남편, 자식에게는 아버지, 부모님에게는 자식, 회사에서는 회사원, 동아리에서는 총무 등 상황과 환경에 따라서 달라지는 것과 비슷하다고 할 수 있다.
객체 지향에서도 다형성도 이와 비슷하다. 즉, 어떤 객체의 속성이나 기능이 그 맥락에 따라 다른 역할을 수행할 수 있다는 객체지향의 특성을 의미한다. 대표적인 예로 우리가 앞서 본 메서드 오바라이딩과 오버로딩이 있다.

**Vehicle interface**

```
public interface Vehicle {
     public abstract void start()
     void moveForward();   // public abstract 키워드 생략 가능
     void moveBackward();
     }
```

**Car Class**

```
public class Car implements Vehicle {
     @Override
      public void moveForward() {
                System.out.println("자동차가 앞으로 전진합니다.");
     }
     @Override
     public void moveBackward() {
              System.out.println("자동차가 뒤로 후진합니다.")
    }
}
```

추상화에서 본 것처럼 메서드 오버라이딩을 사용하면 같은 이름의 moveForward()와 move Backward()를 각각의 클래스의 맥락에 맞게 재정의하여 사용할 수 있다. 즉, 같은 이름의 메서드가 상황에 따라 다른 역할을 수행하는 것이다. 또한, 하나의 클래스 내에서 같은 이름의 메서드를 여러개 중복하여 정의하는 것을 의미하는 메서드 오바로딩도 이와 같은 맥락이라고 할 수 있다.

> 객체지향 프로그래밍에서 다향성이란 한 타입의 참조변수를 통해 여러 타입의 객체를 참조할 수 있도록 만든 것을 의미한다. 좀 더 구체적으로, 상위 클래스 타입의 참조변수로 하위 클래스의 객체를 참조할 수 있도록 하는 것이다.

위의 정의만 봐서는 한번에 이해하기 어렵다. 아래 예제를 통해서 좀 더 쉽게 이해해보도록 해보자.

> 사람이 음식을 먹습니다.
> 여기서 음식은 상황에 따라서 피자가 될 수도, 치킨이 될 수도, 짜장면이 될 수도 있다. 또 한편으로는, 사람은 옆 집의 철수가 될 수도 있고, 영희가 될 수도, 선생님이 될 수도, 내동생이 될 수도 있다. 정리하면, 앞서 설명한 다형성의 맥락과 마찬가지로 음식과 사람은 그 상황에 맥락에 따라서 모습이 바뀔 수 있다.
> 지금까지 사용했던 예시를 들어보면 이동수단은 자동차가 될 수도, 오토바이가 될 수도 있다. 다르게 표현해보면 '자동차는 자동차이다. '라는 명제와 '자동차는 이동수단이다. '라는 명제는 모두 참이다. 오토바이의 경우도 마찬가지이다. 이동수단이라는 범위 안에 자동차와 오토바이는 하나로 묶을 수 있게 된다. 즉, 이동수단은 작은 개념들을 품을 수 잇는 포괄적인 개념이라는 의미이다.

객체지향 프로그래밍에서 다형성이란 앞서 설명한 이동수단과 같은 넓은 범위의 타입, 즉 상위 클래스 타입의 참조 변수로 그것과 관계있는 하위 클래스들을 참조할 수 있는 능력이다.

앞서 상속 파트에서 상위 클래스와 하위 클래스를 상속관계로 만들고, 객체를 생성하여 어떤 속성과 기능을 사용했을 때 우리는 아래와 같이 객체를 생성하였다.

**Main Class**

```
public class Main {
     public static void main(String[] args) {
               Car car = new Car();  //기존에 사용했던 객체 생성 방식
               MotorBike motorBike = new MotorBike();
      }
}
```

이제 당형성 개념을 활용해서 객체를 생성하는 방법을 추가해보자

**Main Class**

```
public class Main {
        public static void main(String[] args) {
               Car car = new Car();  //기존에 사용했던 객체 생성 방식
               MotorBike motorBike = new MotorBike();

               Vehicle car2 = new Car(); //다형성을 활용한 객체 생성 방식
         }
 }
```

위에 코드를 확인해보면, 상위클래스 타입의 참조변수로 하위 클래스 객체를 참조하는 것의 의미를 좀 더 구체적으로 이해할 수 있다. 원래 우리가 사용했던 방식은 하위 클래스의 객체를 생성하여 하위 클래스 타입의 참조변수에 할당해주었지만, 다형성을 활용한 객체 생성방식에서는 하위 클래스의 객체를 생서앟여 하위 클래스 타입의 참조 변수 car2에 할댕해주고 있다. 다형성을 활용하면 여러 종류의 객체를 배열로 다루는 일이 가능해진다.

```
public class Main {
       public static void main(String[] args) {
                  Vehicle vehicles[] = new Vehicle[2];
                  Vehicles[0] = new Car
                  Vehicles[1] = new MotorBike();

                  for (Vehicle vehicle : vehicles) {
                         System.out.println(vehicle.getClass());  // 각각의 클래스를 호출해주는 메서드
                  }
         }
}

//출력값
class Car
class MotorBike
```

상위 클래스 Vehicle 타입의 객체 배열을 생성해주면, 이제 해당 타입의 참조변수는 Vehicle 클래스의 상속 관계에 있는 모든 하위 클래스들을 그 안에 담아줄 수 있다. 다형성을 활용하면 하나의 타입만으로 여러 가지 타입의 객체를 참조할 수 있어 보다 간편하고 유연하게 코드를 작성하는 것이 가능해진다.

**Driver Class**

```
public class Driver {
     void drive(Car car) {
            car.moveForward();
            car.moveBackward();
      }

     void drive(Car car) {
            motorBike.moveForward();
            motorBike.moveBackward();
     }
 }
```

**Main Class**

```
public class Main {
         public static void main(String[] args) {
                 Car car = new Car();
                 MotorBike motorBike = new MotorBike();
                 Driver driver = new Driver();

                 driver.driver(car);
                 driver.driver(motorBike);
         }
}

// 출력값
전진합니다.
후진합니다.
오토바이가 앞으로 전진합니다.
후진합니다.
```

위에 예제에서 알 수 있듯이, Driver 클래스의 코드는 매우 간단하다. 즉, 매개변수로 자동차나 오토바이 객체를 전달받아 운전하는 것이다. 이렇게 하나의 객체가 다른 객체의 속성과 기능에 접근하여 어떤 기능을 사용할 때, 우리는 AClass는 BClass에 의존한다고 표현한다.
같은 맥락에서, 위에 코드 예제를 도식을 표현하면 아래와 같이 그려볼 수 있을 것이고, 우리는 Driver클래스가 Car클래스와 MotorBike 클래스에 의존하고 있다라고 설명할 수 있다. 즉 Driver 클래스와 다른 두개의 클래스가 서로 직접적인 관계를 가지고 있는데 이러한 상황을 객체들간의 결합도가 높다고 표현한다.

![스크린샷 2023-07-31 오후 4 16 09](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/6f9ee149-60a0-4f2b-a1b9-17abc2837c3e)
하지만 결합도가 높은 상태는 객체 지향적인 설계를 하는데 매우 불리하다
만약 지금처럼 이동 수단이 자동차와 오토바이 단 2개가 아니라 수 십, 수백개라면 코드도 수 십번, 수백번 작성해야 할 것이다.

```
public class Driver {
      void drive(Car car) {
              car.moveForward();
              car.moveBackward();
       }
      void drive(MotorBike motorBike) {
              motorBike.moveForward();
              motorBike.moveBackward();
       }
      void drive(Bus bus) {
              bus.moveForward();
              bus.moveBackward();
       }
      void drive(Train train) {
              train.moveForward();
              train.moveBackward();
       }
}
```

MotorBike클래스가 다른 클래스 MotorCycle클래스로 변경되어야 하는 경우는 어떻게 될까?

```
public class Driver {
      void drive(Car car) {
              car.moveForward();
              car.moveBackward();
       }
      void drive(MotorCycle motorCycle) {
              motorCycle.moveForward();
              motorCycle.moveBackward();
       }
}
```

마찬가지로, Driver안에 매개변수로 전달되는 참조변수의 타입과 참조변수를 수정할 수 밖에 벗는 상황이 발생한다. 그리고 코드가 많아질수록 이 작업은 아주 고되고 힘든 작업이 될 수 밖에 없다. 운전자가 운전을 배웠는데 이동수단이 바뀔 때마다 새롭게 운전을 배워야 하는 상황과 같다고 할 수 있다.
객체지향 프로그래밍은 지금까지 공부한 추상화, 상속, 그리고 다형성의 특성을 활용하여 프로그래밍을 설계할 때 역할과 구현을 구분하여 객체들 간의 직접적인 결합을 피하고, 느슨한 관계 설정을 통해 보다 유연하고 변경이 용이한 프로그램 설계를 가능하게 만들었다.
이 부분을 코드로 확인해보자

**Vehicle Interface**

```
public interface Vehicle {   //이동 수단의 역할 정의
        void moveForward();
        void moveBackward();
}
```

**Car Class**

```
public class Car implements Vehicle {
        @Override
         public void moveForward() {
                 System.out.println("자동차가 앞으로 전진합니다." )
        }
        @Override
         public void moveBackward() {
                 System.out.println("자동차가 뒤로 후진합니다." )
        }
}
```

**MotorBike Class**

```
public class MotorBike implements Vehicle {   // 이동수단 인터페이스를 구현
        @Override
         public void moveForward() {
                 System.out.println("오토바이가 앞으로 전진합니다." )
        }
        @Override
         public void moveBackward() {
                 System.out.println("오토바이가 뒤로 후진합니다." )
        }
}
```

**Driver Class**

```
public class Driver {
        void drive (Vehicle vehicle) {   // 매개변수로 인터페이스 타입의 참조변수를 전달.
              vehicle.moveForward();
              vehicle.moveForward();
         }
}
```

**Main Class**

```
public class Main {
        public static void main(String[] args) {
                 Car car = new Car();
                 MotorBike motorBike = new MotorBike();
                 Driver driver = new Driver();

                 driveer.driver(car);
                 driver.driver(motorBike);
        }
}

//출력값
자동차가 앞으로 전진힙니다.
자동차가 뒤로 후진합니다.
오토바이가 앞으로 전진합니다.
오토바이가 뒤로 후진합니다.
```

추상화에서 봤던 것처럼 Vehicle Interface를 통해 이동 수단의 역할을 추상화하고, 각각 Car Class와 MotorBike 클래스에서 기능들을 구현하고 있다.

**Vehicle Interface 적용 전**

```
public class Driver {
      void drive(Car car) {
              car.moveForward();
              car.moveBackward();
      }
      void drive(MotorBike motorBike) {
              motorBike.moveForward();
              motorBike.moveBackward();
      }
      void drive(Bus bus) {
              bus.moveForward();
              bus.moveBackward();
      }
      void drive(Train train) {
              train.moveForward();
              train.moveBackward();
      }
}
```

**Interface 적용 후**

```
public class Driver {
       void drive(Vehicle vehicle) {   //매개변수로 인터페이스 타입의 참조변수를 전달.
              vehicle.moveForward();
              vehicle.moveBackward();
      }
}
```

한눈에 봐도 코드의 중복이 사라지고, 코드가 훨씬 간결해졌다는 사실을 알 수 있다. 핵심은 drive()메서드로 전달되는 매개변수의 타입을 상위 클래스인 인터페이스 타입 Vehicle로 변경한 것이다. 이제 다형성의 세례를 받은 drive() 메서드의 매개변수로 인터페이스를 구현한 객체라면 무엇이든 전달이 될 수 있게 되었다. 이해하기 쉽게 위에 코드를 그림으로 나타내면 아래와 같다.
![스크린샷 2023-07-31 오후 5 10 44](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/74ac4c19-dacb-4552-b301-9b9cbde4f0fc)

앞서 봤었던 도식에는 Driver클래스가 Car와 MtorBike클래스 각각과 직접적으로 ㅇ녀결되어 강한 결합도를 보였지만, 이제는 Vehicle인터페이스를 통해 간접적으로 연결되어 결합도가 낮아졌다. 이제 Driver클래스는 더 이상 각각의 클래스 내부의 변경이나 다른 객체가 새롭게 교체되는 것을 신경 쓰지 않아도 인터페이스에만 의존하여 수정이 있을 때마다 코드 변경을 하지 않아도 된다.
아까의 비유로 표현하면, 운전자가 운전하는 법을 매번 새롭게 배우지 않아도 변경된 이동 수단을 이용하는데 아무런 문제가 발생하지 않는다. 이것이 지금까지 학습한 추상화와 다형성의 특성을 활용한 역할과 구현의 구분이자, 보다 유연하고 변경이 용이한 소프트웨어 설계를 가능하게 하는 객체지향 프로그래밍이라고 할 수 있다.

**Main Class**

```
public class Main {
         public static void main(String[] args) {
                  Vehicle car = new Car(); //높은 결합도
                  Vehicle motorBike = new MotorBike()
                  Vehicle driver = new Drivder()

                  driver.drive(car);
                  driver.drive(motorBike);
        }
}

//출력값
자동차가 앞으로 전진합니다.
자동차가 뒤로 후진합니다.
오토바이가 앞으로 전진합니다.
오토바이가 뒤로 후진합니다.
```

실행 클래스의 코드에서 객체를 생성할 때, new Car()와 new MotorBike()처럼 객체에 직접적으로 의존하고 있어서, 해당 객체를 다른 객체로 변경할 시 코드의 변경이 불가피하다. 즉, 다시 객체 간 높은 결합도를 보이는 상황이 초래되었다.
이 문제를 해결하기 위해서 등장한 것이 바로 의존관계 주입(dependency injection) 이라 부르는 스프링 프레임워크의 핵심적인 개념이다.

객체지향 프로그래밍은 객체 간 관계와 협력을 설계하는 것인데, 다형성은 그 관계를 보다 유연하고 확장이 용이한 설계가 가능하도록 하는데 핵심적인 역할을 한다는 사실이 중요하다. 또한, 다형성을 제대로 활용하기 위해서 앞서 배웠던 추상화와 상속에 대한 내용들이 함께 존재햐야 한다는 사실도 기억해야 한다. 즉, 추상화가 있어야 각 객체들의 역할 정의가 가능하고, 인터페이스는 상위 클래스-하위클래스를 전제하기 때문에 상속에서 배웠던 개념들이 함께 필요하다.

### 4. 캡슐화

캡슐화란 클래스 안에 서로 연관되어 있는 속성과 기능들을 하나의 캡슐로 만들어 데이터를 외부로부터 보호하는 것을 말한다.
자바 객체 지향 프로그래밍에서 캡슐화를 하는 이유는 두가지가 있다

- 데이터 보호(data protection) = 외부로부터 클래스에 정의돈 속성과 기능들을 보호
- - 데이터 은닉(data hiding) = 내부의 동작을 감추고 외부에는 필요한 부분만 노출
    ![스크린샷 2023-07-31 오후 5 23 59](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/75097703-fa10-441c-a34a-0bb5db6562ff)

외부로부터 클래스에 정의된 속성과 기능들을 보호하고, 필요한 부분만 외부로 노출될 수 있도록 하여 각 객체 고유의 독립성과 책임 영역을 안전하게 지키고자 하는 목적이 있다.
자바 객체지향프로그램에서 갭슐화를 구현하기 위한 방법은 두가지가 있다.
첫번째로 접근제어자가 있다, 접근 제어자는 클래스 또는 클래스의 내부의 멤버들에게 사용되어 해당 클래스나 멤버들을 외부에서 접근하지 못하도록 접근을 제한하는 역할을 한다.

![스크린샷 2023-07-31 오후 5 30 03](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/dcd1dd89-84fc-43f2-b046-96fc4d5253e2)

위에 그림은 접근제어자를 우리가 실생활에서 쉽게 접할 수 있는 화장실을 예시로 표현한 것이다. 모두에게 열려 있는 공중화장실, 특정한 멤버십을 가진 사람들에게만 열려있는 호텔 화장실, 그리고 나만 사용할 수 있는 우리집 개인 화장실은 각각 다른 접근 범위를 가진다고 할 수 있다.

접근제어자도 같은 개념이라고 생가갛면 쉽다. 자바에서는 public, default, protected, private총 4가지 종류의 접근 제어자가 있는데 위 화장실의 예제처럼 오른쪽으로 갈 수록 더 좁은 접근 범위를 가진다. 따라서 어떤 소프트웨어 프로그램을 설계할 때 위의 접근 제어자를 활용하여 어떤 클래스나 그 멤버의 대한 접근 범위를 설정하여 데이터를 효과적으로 보호할 수 있다.
![스크린샷 2023-07-31 오후 5 32 58](https://github.com/mandoo1229/React-Board-Restart/assets/123732776/6e74cc7d-4eb9-4051-9af2-88217a0921ef)
위에 표에서 확인할 수 있는 것처럼, 접근 제어자의 접근 범위가 각각 클래스 내, 패키지 내, 다른 패키지의 하위 클래스, 그리고 패키지 외까지 각각 다른 것을 확인할 수 있다.

**SuperClass**

```
package package1;
class Test {
        public static void main(String[] args) {
                  SuperClass superClass = new  SuperClass();

          // System.out.println(parent.a);     //동일 클래스가 아니기 때문에 에러 발생
          System.out.println(superClass.b);
          System.out.println(superClass.c);
          System.out.println(superClass.d);
          }
}

public class SuperClass {
         private int a = 1;
         int b = 2;
         protected int c = 3;
         public int d = 4;

         public void printEach() {
                System.out.println(a);
                System.out.println(b);
                System.out.println(c);
                System.out.println(d);
          }
}

// 출력값
2
3
4
```

다른 패키지 Test Class

```
package package2;  //package2
import package1.SuperClass;

class SubClass extends SuperClass {   // package1로부터 SuperClass 클래스를 상속
        public void printEach() {
                // System.out.println(a) // 에러 발생
                // System.out.println(b) // 에러 발생
                System.out.println(c) // 다른 패키지의 하위 클래스
                System.out.println(d)
       }
}

public class Test2 {
        public static void main(String[] args) {
                SuperClass parent = new SuperClass();

                   // System.out.println(parent.a); // public을 제외한 모든 호출 에러
                  // System.out.println(parent.b);
                  // System.out.println(parent.c);
                   System.out.println(parent.d);
          }
}
```

자바의 캡슐화를 구현하기 위한 두 번째 방법으로는 getter / setter 메서드가 있다.

**Car Class**

```
public class Car {
       private String model;
       private String color;
       private int wheels;

       public String getModel() {
                return model;
        };
       public String getModel(String model) {
                this.model = model;
        };
       public void setColor(String color) {
                return color;
        };
       public void getColor(String color) {
                this.color = color
        };
       public int getWheels() {
                return wheels;
        };
       public void setWheels(int wheels) {
                this.wheels = wheels;
        };
}
```

위에 예제를 보면, 모든 속성값들이 private 접근 제어자로 선언되어 있고, getter/setter 메서드의 접근 제어자만이 public으로 열려 있다. 따라서 선택적으로 외부에 접근을 허용할 속성과 그렇지 않을 속성을 getter/setter 메서드를 통해 설정해줄 수 있다.

**Car class**

```
public class Car {
     private String model;
     private String color;

    public Car(String model, String color) {
            this.model = model;
            this.color = color;
     }
     public void startEngine() {
            System.out.println("시동을 겁니다.");
     }
     public void moveForward() {
            System.out.println("자동차가 앞으로 전진합니다.");
     }
     public void openWindow() {
            System.out.println("모든 창문을 엽니다.");
     }
}
```

**Driver Class**

```
public class Driver {
       private String name;
       private Car car;

       public Driver(String name, Car car) {
              this.name = name;
              this.car = car;
       }

       public void drive() {
               car.startEngine();
               car.moveForward();
               car.openWindow();
       }
}
```

**Main Class**

```
public class Main {
        public static void main(String[] args) {

               Car car = new Car("테슬라 모델X", "레드");
               Driver driver = new Driver("남민우", car);

               Driver.drive();
         }
}

//출력값
시동을 겁니다.
자동차가 앞으로 전진합니다.
모든 창문을 엽니다.
```

위에 코드는 아무런 문제 없이 잘 동작하는 코드처럼 보이지만, 치명적인 약점을 가지고 있다. Driver Class의 drive()메서드의 바디를 살펴보면, 해당 메서드가 호출되었을 때 Car Class의 메서드들이 순차적으로 실행되고 있는 것을 확인할 수 있다.

겉으로 봤을 때는 아무런 문제가 없어 보이지만 왜 치명적일까?

만약 Car클래스의 3가지 메서드들에 어떤 변경이 생겼다고 가정해보자. 그러면 해당 메서드들을 사용하고 있는 Driver Class의 drive()메서드의 수정이 불가피하다. 다른말로, Driver Class가 Car Class의 세부적인 내부 로직을 속속히 너무 잘 알고 있고, 이것은 우리가 피하고자 했던 객체간의 결합도가 높은 상태를 의미한다.

이럴 때 우리는 캡슐화를 활용하여 객체의 자율성, 즉 하나의 객체가 해당 객체의 속성과 기능에 대한 독점적인 책임을 담당하도록 만들고, 이를 통해 객체 간의 결합도를 낮게 유지할 수 있다.

**Car Class**

```
public class Car {
      private String model;
      private String color;

      public Car (String model, String color) {
             this.model = model;
             this.color = color;
      }
      private void startEngine() {
             System.out.println("시동을 겁니다.");
      }
      private void moveForward() {
             System.out.println("자동차가 앞으로 전진합니다.");
      }
      private void openWindow() {
             System.out.println("모든 창문을 엽니다.");
      }

      public void operate() {    // 앞서 Driver 클래스에 정의된 메서드를 이용해 메서드 추출
              startEngine();
              moveForward();
              openWindow();
      }
}
```

**Driver Class**

```
public class Driver {
       private String name;
       private Car car;

       public Driver (String name, Car car) {
               this.name = name;
               this.car = car;
       }
       public String getName() {
               return name;
       }
       public void drive() {
              var.operate();
       }
}
```

**Main Class**

```
public class Main {
       public static void main(String[] args) {
            Car car = new Car("테슬라 모델 X", "레드");
            Driver driver = new Driver("남민우", car);
            driver.drive();
      }
}

//출력값
시동을 겁니다.
자동차가 앞으로 전진합니다.
모든 창문을 엽니다.
```

아까와 출력값은 동일하지만, 기존의 Driver Class가 하나 하나 호출해줐던 메서드들을 모두 operate() 메서드로 묶어 Car Class로 옮겨두었고, Driver Class내에서는 내부 동작을 전혀 신경쓰지 않아도 단순히 operate() 메서드를 호출하여 사용하고 있다.

또한, operate()메서드 내부의 메서드들은 외부에서 호출되어 사용할 일이 없으므로 접근 제어자를 모두 private으로 변경해주었다. 정리하면, Car Class와 관련되 기능들은 온전히 Car에서만 관리되도록 하였고, 불필요한 내부 동작의 노출을 최소화하였다. Driver Class입장에서는 더 이상 Car Class의 내부 로직을 알지 못하고, 알 필요도 없어졌다.
캡슐화를 활용하면, 객체 내부의 동작의 외부로의 노출을 최소화화여 각 객체의 자율성을 높이고, 이를 통해 객체 간 결합도를 낮추어 앞서 설명한 객체 지향의 핵심적인 이점을 잘 살리는 방법으로 프로그램을 설계하는 일이 가능하다.
