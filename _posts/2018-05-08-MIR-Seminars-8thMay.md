---
layout: post
title: "Seminários MIR: Gerenciamento de Recursos e Planejamento/Simulação de Desastres"
date: 2018-05-08
---

<pre>
Nesta semana na sequência dos Seminários internos do MIR de 2018 teremos apresentações
sobre planejamento e simulação de desastres, assim como gerenciameto  de recursos para 
robótica móvel embarcada. 

Após as apresentações haverá discussões sobre os temas abordados.
 
Data: 08/05/2018
Horário: 14h00
Local: P32, mini auditório 207

Agenda:
=======


Apresentador: Marcelo Paravisi
Título: Toward Accurate Hydrologic Urban Flooding Simulations for Disaster Robotics
Abstract: 
Testing and benchmarking robots in actual disaster scenarios is risky and sometimes 
nearly impossible. The lack of adequate tests could make robots more vulnerable and 
less effective in an actual disaster situation. However, even if it was possible to 
test them in a disaster scenario, the test itself would have high risks for the equip-
ment and the robot operator. For this reason, simulations can be a powerful alternative 
to validate unmanned systems in safe and controlled virtual environments.  The main 
challenge is to devise an accurate virtual scenario as close as possible to an actual 
disaster scenario. This problem is particularly harder if the robot in  question is an 
unmanned surface vehicle (USV), mainly due to the numerous disturbances which can affect
the robot. This paper presents and discusses the simulation of an urban flooding scenario 
with accurate environmental disturbances faced by an USV, such as water currents, waves 
and winds. Results demonstrate that these environmental disturbances have a relevant 
effect on the USV's ability to perform basic navigational tasks. The main conclusion of 
this work is that there is a long road ahead of USV simulators in order to validate USVs 
in realistic disaster scenario simulations.
Duração (estimativa): 20 minutos


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
Duração (estimativa): 20 minutos


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
Duração (estimativa): 30min

</pre>
