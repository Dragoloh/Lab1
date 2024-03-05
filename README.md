# Lab1
using System;

class ChildrenOfTheForest
{
    private string forestDatabase;

    public ChildrenOfTheForest(string database)
    {
        forestDatabase = database;
    }

    public void Speak()
    {
        Console.WriteLine("Дети леса заговаривают");
    }

    public void PerformRitual()
    {
        Console.WriteLine("Дети леса проводят ритуал");
    }

    public void Dance()
    {
        Console.WriteLine("Дети леса танцуют");
    }
}

class WhiteWalkers
{
    private string walkerDatabase;

    public WhiteWalkers(string database)
    {
        walkerDatabase = database;
    }

    public void GatherArmyOfTheDead()
    {
        Console.WriteLine("Белые ходоки собирают армию мертвецов");
    }

    public void MarchToBattle()
    {
        Console.WriteLine("Белые ходоки идут на битву");
    }

    public void Freeze()
    {
        Console.WriteLine("Белые ходоки замораживают все вокруг");
    }
}

class People
{
    private string peopleDatabase;

    public People(string database)
    {
        peopleDatabase = database;
    }

    public void Talk()
    {
        Console.WriteLine("Люди разговаривают");
    }

    public void Eat()
    {
        Console.WriteLine("Люди едят");
    }

    public void Work()
    {
        Console.WriteLine("Люди работают");
    }
}

class Giants : People
{
    private string giantDatabase;

    public Giants(string database) : base(database)
    {
        giantDatabase = database;
    }

    public void Smash()
    {
        Console.WriteLine("Великаны разбивают все на части");
    }

    public void Roar()
    {
        Console.WriteLine("Великаны ревут");
    }

    public void Sleep()
    {
        Console.WriteLine("Великаны спят");
    }
}

class Constructors
{
    public static void Run()
    {
        Console.WriteLine("Введите название базы данных:");
        string database = Console.ReadLine();

        Console.WriteLine("Выберите класс (ДетиЛеса, БелыеХодоки, Люди, Великаны):");
        string selectedClass = Console.ReadLine().ToUpper();

        switch (selectedClass)
        {
            case "ДЕТИЛЕСА":
                ChildrenOfTheForest children = new ChildrenOfTheForest(database);
                Console.WriteLine("Выберите функцию (Speak, PerformRitual, Dance):");
                string selectedFunctionChildren = Console.ReadLine().ToUpper();
                switch (selectedFunctionChildren)
                {
                    case "SPEAK":
                        children.Speak();
                        break;
                    case "PERFORMRITUAL":
                        children.PerformRitual();
                        break;
                    case "DANCE":
                        children.Dance();
                        break;
                    default:
                        Console.WriteLine("Неверный выбор функции.");
                        break;
                }
                break;
            case "БЕЛЫЕХОДОКИ":
                WhiteWalkers walkers = new WhiteWalkers(database);
                Console.WriteLine("Выберите функцию (GatherArmyOfTheDead, MarchToBattle, Freeze):");
                string selectedFunctionWalkers = Console.ReadLine().ToUpper();
                switch (selectedFunctionWalkers)
                {
                    case "GATHERARMYOFTHEDead":
                        walkers.GatherArmyOfTheDead();
                        break;
                    case "MARCHTOBATTLE":
                        walkers.MarchToBattle();
                        break;
                    case "FREEZE":
                        walkers.Freeze();
                        break;
                    default:
                        Console.WriteLine("Неверный выбор функции.");
                        break;
                }
                break;

case "ЛЮДИ":
                People people = new People(database);
                Console.WriteLine("Выберите функцию (Talk, Eat, Work):");
                string selectedFunctionPeople = Console.ReadLine().ToUpper();
                switch (selectedFunctionPeople)
                {
                    case "TALK":
                        people.Talk();
                        break;
                    case "EAT":
                        people.Eat();
                        break;
                    case "WORK":
                        people.Work();
                        break;
                    default:
                        Console.WriteLine("Неверный выбор функции.");
                        break;
                }
                break;
            case "ВЕЛИКАНЫ":
                Giants giants = new Giants(database);
                Console.WriteLine("Выберите функцию (Talk, Eat, Smash, Roar, Sleep):");
                string selectedFunctionGiants = Console.ReadLine().ToUpper();
                switch (selectedFunctionGiants)
                {
                    case "TALK":
                        giants.Talk();
                        break;
                    case "EAT":
                        giants.Eat();
                        break;
                    case "SMASH":
                        giants.Smash();
                        break;
                    case "ROAR":
                        giants.Roar();
                        break;
                    case "SLEEP":
                        giants.Sleep();
                        break;
                    default:
                        Console.WriteLine("Неверный выбор функции.");
                        break;
                }
                break;
            default:
                Console.WriteLine("Неверный выбор класса.");
                break;
        }
    }
}

class Program
{
    static void Main(string[] args)
    {
        Constructors.Run();
    }
}
