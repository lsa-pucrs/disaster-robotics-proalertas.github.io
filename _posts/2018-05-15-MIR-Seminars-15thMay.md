---
layout: post
title: "Seminários MIR: Gerenciamento de Recursos e Planejamento/Simulação de Desastres PARTE II"
date: 2018-05-15
---

<pre>
Continuaremos os seminários não realizados da semana passada sobre planejamento simbólico/
geométrico em caso de desastres e gerenciameto de recursos para robótica móvel embarcada. 

Após cada apresentação haverá discussões sobre os temas abordados.
 
Data: 15/05/2018
Horário: 14h00
Local: P32, sala 516

Agenda:
=======

Apresentador: Renan Guedes Maidana
Título: Autonomic Computing Towards Resource Management in Embedded Mobile Robots
Abstract:
Small and lightweight robots are becoming a reality due to the increasing pervasiveness 
of embedded computers. However, much of the research in mobile robotics is focused  on 
increasing the robots' autonomy, disregarding the computational limitations of embedded 
computers. The area of autonomic computing defines self-managing systems, also known as 
autonomic systems, which manage computational resources (e.g. CPU load) and reduce the 
effect of processing bottlenecks, as well as alleviating energy consumption in embedded 
mobile robots. In this paper, we propose the use of autonomic systems with control theory 
for resource management in embedded mobile robots. Our expected contribution is to use 
autonomic computing to develop self-contained embedded robots, capable of operating with 
few embedded computers and without the aid of external servers. We implement an autonomic 
system which successfully controls the latency and CPU load of a dense optical flow appli-
cation, running on a Raspberry Pi 2 embedded computer, which validates the proposed idea.
Duração (estimativa): 45min


Apresentador: Mauricio Cecilio Magnaguagno
Título: Symbolic-Geometric planning for disaster/rescue situations
Abstract:
Classical planners, with actions described with preconditions and effects, create a way to 
operate on (mostly) purely symbolic models in order to find plans to reach an agent's goals.
Plans found by classical planners often lack the geometric and temporal details required to 
solve motion problems, such as grasping an object or avoiding collisions with moving objects.
Such details include robot dimensions and object properties.
A  possible  approach  is to mix off-the-shelf classical and motion planners and share data 
between the parts, which generates a large search-space without significant relations between 
the objects. In order to tackle this problem, we need a custom symbolic-geometric planner to 
share and  limit possible values as planning progresses, to minimize memory usage and planning 
time.
To better limit which data must be considered we can describe search paths as strategies to 
force the planner to consider  certain user  preferences to obtain a faster solution with a 
better plan quality. This is specially important in emergency response planning as  rescue 
teams may include people  that already have certain methods to operate, and robotic agents 
(new team members) must match an expected behavior to increase the efficiency of the team.
In this seminar we explain the advantages of HTN planning over classical approaches, how data 
can be shared between the symbolic and geometric parts while considering temporal constraints 
described to the system, and some applications in disaster/rescue situations.
Duração (estimativa): 45min

</pre>
