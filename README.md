Feature: ADA ramp finder
	In order to find the nearest ADA ramp
	Visually impaired users must be alerted to where the 
	nearest ramp is
	
Scenario: A user is a quarter of the way to the ramp
	Given a beacon has been placed on or near the ADA
	ramp
	When a blind user is a quarter of the way to the ramp
	Then I should hear a beep (not too loud) notifying me 
	that I am a quarter of the way to the ramp

Scenario: A user is halfway to the ramp
	Given a beacon has been placed on or near the ADA
	ramp
	When a blind user is halfway to the ramp
	Then I should hear a beep (slightly louder) notifying
	me that I am halfway to the ramp

Scenario: A user is three-fourths of the way to the ramp
	Given a beacon has been placed on or near the ADA 
	ramp
	When blind user is three-fourths of the way to the ramp
	Then I should hear a beep (even louder) notifying me
	that I am three-fourths of the way to the ramp

Scenario: A user has finally reached the ramp
	Given a beacon has been placed on or near the ADA 		ramp
	When the user is at the starting point of the ramp
	Then I should hear a beep notifying me that I am at		the ramp 
	At this point, the beacon should be fairly loud

Scenario: A user approaches a left turn while on the ramp
	Given a beacon has been placed at the left turn
	When the user is at the left turn on the ramp
	Then I should hear a beep notifying me that I need to 
	make a left turn

Scenario: A user approaches a right turn while on the ramp
	Given a beacon has been placed at the right turn
	When the user is at the right turn on the ramp
	Then I should hear a beep notifying me that I need to
	make a right turn

Scenario: A user reaches the bottom of the ramp
	Given a beacon has been placed at the bottom of the 
	ramp
	When the user has reached the bottom of the ramp
	Then I should hear a beep notifying me that I have
	safely reached the bottom of the ramp

Scenario: A user is about to exit the vehicle
	Given a beacon has been placed at the top of the ramp
	When the user has reached the ramp to exit the vehicle
	Then I should hear a beep notifying me I have reached
	The ramp and I can safely exit the vehicle

Scenario: A user is about to exit the vehicle
Given there is no beacon placed to the left of the ramp
When the user has reached the ramp to exit the vehicle
Then I should make his way to the right side of
the ramp until he hears a beep signifying him of the ramp’s location

Scenario: A user is about to exit the vehicle
Given there is no beacon placed to the right of the ramp
When the user has reached the ramp to exit the vehicle
Then I should make his way to the left side of the ramp until he hears a beep signifying him of the 
ramp’s location 
