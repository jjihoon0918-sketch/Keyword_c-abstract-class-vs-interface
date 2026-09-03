# Keyword_c-abstract-class-vs-interface

- C# Abstract Class vs Interface

abstract class와 interface는 모두 추상화를 위해 사용하지만 목적이 다르다.

- Abstract Class

  **공통된 상태와 기능을 공유할 때 사용한다.**

  - 필드, 프로퍼티, 생성자를 가질 수 있음
  - 일반 메서드와 abstract 메서드를 함께 사용 가능
  - 클래스는 하나만 상속 가능
  - is-a 관계에 적합

  abstract class Animal
 {
    public string Name { get; set; }

    public abstract void Speak();

    public void Sleep()
    {
        Console.WriteLine("Sleep");
    }
  
 }

  class Dog : Animal
 {
    public override void Speak()
    {
        Console.WriteLine("멍멍");
    }
 }
- Interface

  **특정 기능을 구현하도록 규칙을 정할 때 사용한다.**

  - 여러 인터페이스를 동시에 구현 가능
  - 서로 관련 없는 클래스에도 같은 기능을 부여할 수 있음
  - 인스턴스 필드나 생성자는 가질 수 없음
  - can-do 관계에 적합

 interface IRunnable
 {
    void Run();
 }

 class Dog : IRunnable
 {
    public void Run()
    {
        Console.WriteLine("달린다.");
    }
 }

 - **차이점**
 - Abstract Class	Interface
 - 공통 상태와 기능 공유	기능에 대한 규칙 정의
 - 하나만 상속 가능	여러 개 구현 가능
 - 필드, 생성자 사용 가능	인스턴스 필드, 생성자 사용 불가
 - is-a 관계	can-do 관계

- 한 줄 정리

Abstract Class → 공통된 특징과 기능을 공유할 때
Interface → 특정 기능을 구현하도록 규칙을 정할 때