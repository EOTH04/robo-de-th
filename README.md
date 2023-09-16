# robo-de-th
package thdaspaty;
import robocode.*;
import java.awt.Color;

/**
 * thbot - a class by (robô de th)
 */
public class Thbot extends Robot{
public void run (){
	setColors(Color.green,Color.black,Color.blue,Color.red,Color.green);
	while (true) {
			ahead(100);
			turnRight(90);
			ahead(100);
			turnLeft(90);
			ahead(100);
		}
	}
	public void onScannedRobot (ScannedRobotEvent e){
	String robotank = e.getName();
	double distancia = e.getDistance();
	System.out.println(robotank + " distancia " + distancia);
	if (distancia < 135)	{
		fire(3);
	}	else {
		fire(1);
	}
	//fire(1.7);
	}
	public void onHitWall(HitWallEvent e){
		back(50);
		turnRight(90);
	}
}

