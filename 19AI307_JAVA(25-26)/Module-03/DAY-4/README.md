# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.
<img width="300" height="116" alt="image" src="https://github.com/user-attachments/assets/2b82a1bc-596b-4f9a-976d-c507a3744030" />

## AIM:
A programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

## ALGORITHM :
1.Start
2.Create an interface WeatherBot with a method:
3.Create TemperatureBot class:
4.Implement the getPrediction() method
5.Create RainfallBot class:
6.Return a rainfall prediction
7.Create WindBot class:
8.Return a wind prediction
9.Create objects of TemperatureBot, RainfallBot, and WindBot
10.Print the predictions
11.End

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Lokesh Rahul V V
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface WeatherBot 
{
    String predict(int temperature);
}

class SunBot implements WeatherBot 
{
    public String predict(int temperature) 
    {
        return (temperature > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot 
{
    public String predict(int temperature) 
    {
        return (temperature < 20) ? "COLD" : "WARM";
    }
}
public class WeatherPrediction 
{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();
        WeatherBot bot;
        if (botType == 1) 
        {
            bot = new SunBot();
        } 
        else if (botType == 2) 
        {
            bot = new RainBot();
        } 
        else 
        {
            System.out.println("Invalid bot type");
            return;
        }

        System.out.println(bot.predict(temperature));
    }
}
```

## OUTPUT:
<img width="458" height="149" alt="Screenshot 2025-11-21 143837" src="https://github.com/user-attachments/assets/c41df431-90bf-4713-b7a3-6296c2627c4f" />

## RESULT:
All bots successfully implement the WeatherBot interface and provide their own customized predictions.
