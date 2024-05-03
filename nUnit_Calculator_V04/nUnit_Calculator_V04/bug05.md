# 💩 bug

````ps
nUnit_Calculator_V02.T004_Calculator.Add_TwoNumbers_ReturnsSum
````

````csharp

using NUnit.Framework;
namespace nUnit_Calculator_V02;


[TestFixture] // Attribut funktioniert nur mit dem nUnit Framework und einer class Definition

public class T004_Calculator

{
    [Test]
    public void Add_TwoNumbers_ReturnsSum()
    {
        // Arrange
        var calculator = new Calculator();
        var x = 2;
        var y = 3;

        // Act
        calculator.Add(x, y);

        // Assert
        Assert.ReferenceEquals(5, calculator.Value);
    }
}

public class Calculator
{
    private int _value;

    public int Value { get { return _value; } }

    public void Add(int x, int y)
    {
        _value = x + y;
    }
}
````