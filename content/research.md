---
title: "Research"
slug: "research"
license: PUBLIC
date: "2019-02-28"
menu:
    main:
        weight: 1
        params: 
            icon: home-search
---

Batteryless Systems collect small amounts of sporadic energy from the surrounding environment and use it to perform complex tasks. My research methodology advocates modular and reusable design. In harvesting-based systems, this means decoupling the environment from the application. More precisely, the transducer’s voltage and current are made independent from those in the application circuit. By doing so, it becomes possible to optimize the energy harvesting input and application circuit’s output independently and simultaneously. The design techniques I have proposed proved to be powerful enough to process data streams from sensors and broadcast results wirelessly. Thanks to advanced energy management and distribution mechanisms, this device needs less than 10 micro-Watts of input power to operate. My research in this domain has been applied to commercial, open-source products like the [miroCard](https://mirocard.swiss/).

![img](https://andresgomez.ch/web/wp-content/uploads/2022/01/mirocard_closeup-removebg-preview.png)



### Physically Enforced Privacy:

Privacy is an ever-growing concern with the proliferation of sensing devices. In the context of mobile devices, for example, battery-powered devices like smartphones can record clear and understandable audio, even if the device is hidden away in a pocket or bag. Mains-powered devices such as Amazon’s Alexa or Google’s Home assistants are designed to continuously listen for activation words before recording audio. However, many phrases can accidentally trigger recordings. Even with privacy protections in place, software-based policies are prone to errors: [accidental updates](https://mashable.com/article/google-assistant-microphone-smoke-alarm) have changed the way these devices wake up. All electronic sensing devices, even batteryless ones, need an energy supply to work. Since batteryless sensors operate from the assumption of an intermittent supply, they can efficiently operate when energy is being harvested and also guarantee complete power-down when there is no harvested energy. As such, a simple physical action from a user like covering a solar panel can ensure that the sensing device is completely off and physically unable to operate. In principle, it is very similar to the privacy-enabling camera shutters found in many laptops, but it goes a step further. A simple visual inspection can ensure users that devices cannot physically turn on.

![img](https://andresgomez.ch/web/wp-content/uploads/2022/01/physical_cover_batteryless-552x1024.jpg)

### Indoor Photovoltaic Harvesting:

The first step to understand the possibilities, and limitations of energy-driven sensing, is to quantify the environment’s primary energy. Photovoltaic transducers (i.e., solar cells) are known to have a very high power density. In indoor environments, solar cells produce energy from natural light when close to a window, artificial light when close to lamps, or a combination of the two. In all cases, however, the amount of harvested energy changes in time spans of seconds, minutes, and hours. At ETH Zurich, we initiated a measurement campaign to study indoor photovoltaic harvesting and its variability. The [2+ year dataset](https://zenodo.org/record/3715472) gathered in an office building is publicly available. The building’s floor plan shows where the solar cells were deployed with energy measuring devices. The violin plots show the distribution of daily harvested energy at four locations, two of which were close to windows and received more energy: nodes C and D. Even though it is indoors, the effects from the sun are visible: node D, whose window was facing east, received most of its daily energy in the morning, while node C received it in the evening.

![img](https://andresgomez.ch/web/wp-content/uploads/2022/01/floorplan-removebg-preview.png)

![img](https://andresgomez.ch/web/wp-content/uploads/2022/01/daily_energies-1.png)



### Real-Time Scheduling

In the real-time domain, computing systems must not only be functionally correct but also respect precise time constraints. Of the many factors that can affect the response time of these systems, the most influential is the arbitration scheme of limited resources: the scheduling algorithm. For my master thesis, I developed Scheduling Framework For Fast Prototyping (SF3P), an application-level framework for prototyping and composing different real-time schedulers. SF3P introduces a new layer at the application level that implements different scheduling algorithms to be used by SF3P tasks running on top of it. This would not be possible in a standard Linux system because the Linux scheduler is priority-based, and has limited scheduling options. Naturally, since SF3P itself runs on top of the standard pthread library, all algorithms must be implemented using a priority-based mechanism.

![img](https://andresgomez.ch/web/wp-content/uploads/2021/12/sf3p.png)