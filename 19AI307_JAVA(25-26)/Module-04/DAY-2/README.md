# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
A smart city has a grid of sensors installed across various zones to monitor Air Quality (AQI).

There are multiple SmartControllers subscribed to this network. Each SmartController is responsible for a specific AQI range:

GreenZoneController: AQI < 100

AlertZoneController: AQI between 100 and 200

DangerZoneController: AQI > 200

When a sensor reports data, only the relevant controller(s) should be notified based on the AQI.

What Students Must Do:
Implement the Observer pattern

SensorNetwork = Subject

Each SmartController = Observer

Each controller decides if it should react to a reported AQI (based on range)

When SensorNetwork receives data, it notifies only relevant observers

Input Format:
First line: Integer n – number of AQI readings

Next n lines: Each line contains: SensorID AQI_value

Output Format:
For each AQI:

Sensor [SensorID] reports AQI: [value]
[Controller]: Taking appropriate action
...
Only relevant controllers should react to the AQI.
<img width="866" height="258" alt="image" src="https://github.com/user-attachments/assets/917aa744-563d-4782-b346-9f44b825d702" />

## AIM:
To implement the Observer Design Pattern where:

SensorNetwork acts as the Subject

SmartControllers act as Observers

Only the relevant controllers (based on AQI range) should respond when an AQI reading is reported.


## ALGORITHM :
1.Start

2.Create an Observer interface with a method update(String sensorID, int value).

3.Create three observer classes:

GreenZoneController → reacts when AQI < 100

AlertZoneController → reacts when 100 ≤ AQI ≤ 200

DangerZoneController → reacts when AQI > 200

4.Create a SensorNetwork (Subject) class:

Maintain a list of observers.

Provide addObserver() and removeObserver() methods.

Provide notifyObservers(sensorID, aqiValue) that sends updates
only to relevant controllers.

5.In main():

Initialize the SensorNetwork.

6.Add all controller observers.

7.Read number of AQI readings: n

8.For each reading:

Read sensorID and AQI value.

9.Print:
Sensor [sensorID] reports AQI: [value]

Call SensorNetwork.notifyObservers(sensorID, value)

Each controller checks the AQI range inside its own update() method:

If AQI matches its range → print action message

10.Else → do nothing

11.End
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Lokesh Rahul V V 
RegisterNumber:  212222100024
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Observer {
    void check(int aqi, String sensorId);
}

class GreenZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi < 100) {
            System.out.println("[GreenZoneController]: AQI is good at Sensor " + sensorId + ". No action needed.");
        }
    }
}

class AlertZoneController implements Observer {
     public void check(int aqi, String sensorId) {
        if (aqi >= 100 && aqi <= 200) {
            System.out.println("[AlertZoneController]: Moderate AQI at Sensor " + sensorId + ". Send public health alert.");
        }
    }
}

class DangerZoneController implements Observer {
     public void check(int aqi, String sensorId) {
        if (aqi > 200) {
            System.out.println("[DangerZoneController]: Critical AQI at Sensor " + sensorId + "! Trigger lockdown protocol.");
        }
    }
}

class SensorNetwork {
    private List<Observer> observers = new ArrayList<>();
    public void register(Observer o) {
        observers.add(o);
    }
    public void receiveData(String sensorId, int aqi) {
        System.out.println("Sensor " + sensorId + " reports AQI: " + aqi);
        for (Observer o : observers) {
            o.check(aqi, sensorId);}
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        SensorNetwork network = new SensorNetwork();

        network.register(new GreenZoneController());
        network.register(new AlertZoneController());
        network.register(new DangerZoneController());

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().split(" ");
            String id = parts[0];
            int aqi = Integer.parseInt(parts[1]);
            network.receiveData(id, aqi);
        }
    }
}
```

## OUTPUT:
<img width="1240" height="256" alt="image" src="https://github.com/user-attachments/assets/7a3f4083-f640-465f-b30c-f0d72e040e87" />

## RESULT:
The program successfully implements the Observer pattern, where the SensorNetwork notifies only the appropriate SmartControllers based on the AQI ranges.
