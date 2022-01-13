```
package jb;
import robocode.HitRobotEvent;
import robocode.ScannedRobotEvent;
import robocode.*;
import java.awt.Color;

// API help : https://robocode.sourceforge.io/docs/robocode/robocode/Robot.html

/**
 * BaddieBot - a robot by (your name here)
 */
public class BaddieBot extends Robot
{
	/**
	 * run: BaddieBot's default behavior
	 */
	public void run() {
		// Initialization of the robot should be put here

		// After trying out your robot, try uncommenting the import at the top,
		// and the next line:

		 setColors(Color.red,Color.blue,Color.red); // body,gun,radar

		// Robot main loop
		while(true) {
			// Replace the next 4 lines with any behavior you would like
			ahead(200);
			fire(1);
			turnLeft(80);
			fire(2);
		}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		// Replace the next line with any behavior you would like
		if (!e.isSentryRobot()) {
            fire(3);
			back(4);
			fire(1);
        }else{
		turnLeft(120);
		fire(2);
		back(40);
		}
	}
	
	public void HitRobotEvent(){
		fire(2);
		turnRight(40);
	}
	/**
	 * onHitByBullet: What to do when you're hit by a bullet
	 */
	public void onHitByBullet(HitByBulletEvent e) {
		// Replace the next line with any behavior you would like
		fire(2);
		turnLeft(-60);
		ahead(10);
		fire(2);
	}
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		// Replace the next line with any behavior you would like
		back(20);
		turnLeft(180);
		ahead(40);
	}
```
