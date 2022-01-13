# BattleBots
package jb;
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

		 setColors(Color.red,Color.blue,Color.red); // body,gun,radar

		// Robot main loop
		while(true) {
			// Replace the next 4 lines with any behavior you would like
			fire(1);
			ahead(200);
			turnGunRight(40);
			back(80);
		}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		// Replace the next line with any behavior you would like

	   	fire(2);
		back(10);
		fire(2);
	}
	/**
	 * onHitByBullet: What to do when you're hit by a bullet
	 */
	public void onHitByBullet(HitByBulletEvent e) {
		// Replace the next line with any behavior you would like
		fire(1);
		turnLeft(-60);
		ahead(10);
	}
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		// Replace the next line with any behavior you would like
		back(20);
		turnLeft(180);
		ahead(10);
	}	
}
