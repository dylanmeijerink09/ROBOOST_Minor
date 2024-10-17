# Chapter 1
```plantuml

@startuml
actor Students
actor ResearchersSaxion
actor TeachersSmeot

entity TechYourFuture
entity MinorIndustrialAutomation

usecase WeldingStation
component WeldingRobot
component KuKaRobot
component DoosanRobot
component AMR

usecase vision
usecase/ "welding/" 

Students -- MinorIndustrialAutomation : Following the minor
ResearchersSaxion -- TechYourFuture : Designing a module for level 3 students in robotics
TeachersSmeot -- TechYourFuture : Designing a module for level 3 students in robotics

MinorIndustrialAutomation -- TechYourFuture : Assisting in designing a module for level 3 students in robotics

TechYourFuture -- WeldingRobot : Welding a item
TechYourFuture -- DoosanRobot : Assist the welding robot
TechYourFuture -- KuKaRobot : Select the right components for the robot with the use of vision

DoosanRobot -- WeldingStation : Assist the welding robot
WeldingRobot -- WeldingStation : Welding a "Thor" hammer

KuKaRobot -- AMR : Brings selected components to on the AMR
AMR -- WeldingStation : Brings components to the welding robot

WeldingStation -- "welding/"
KuKaRobot -- vision
@enduml

