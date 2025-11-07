# 2025-Gyro-Drive-Spike-Python
This repo will contain the new Spike Prime Python of the FLL Tools for Spike Prime 3.0 Robots used in FIRST LEGO League Challenge. This version incorporates all the goodies from the blocks version plus severl features unavailable in Blocks. This is a project to provide updated pre-packaged, tested and working on Spike Prime Python for FLL Challenge teams. 

We encourage you to immediately start learning Spike Python by access this on-line version for the [Spike Python Knowledge Base](https://spike.legoeducation.com/prime/help/lls-help-python#lls-help-python). This is the same information you would see in the hub, without the need for the Hub itself. Become Pythonic over the summer. 

## New Version is Multi Motor Movement support
The newly upload version support multi movement of spinny motors while driving.
Code Example:
'''
    #spinny examples
    front_lift.run(100,25)                      # spin arm up
    sleep(2)
    front_lift.run(0,50)                        # spin arm down

    sleep(2)
    # in this case we want the arms to move while
    # we drive. This can save a lot of time.
    # asunc_op says do not spin the motors youself.
    front_lift.run(100,25, async_op = True)             #set front to go up
    rear_lift.run(100,10, async_op = True)              #set back to go up

    # Now we call gyro_drive. Because there is a list, 
    # gyro_drive will call the static spinny method 
    # spinny.spin_multi_motors in each loop it will 
    # tell the spinnys to move
    # Warning: You MUST make sure that the arms are done
    # before the drive is done. With gyro_drive we are 
    # unable to easily stop the spinnys
    gyro_drive('d', 50, 30,                             # set drive parameters
        spinny_list= [front_lift, rear_lift] )          # and pass a list of spinnys

    sleep(2)
    # imaging using this at the end of your run
    front_lift.run(0,80, async_op = True)               # set front are to go down
    rear_lift.run(0,80, async_op = True)                # set back are to go down
    # the spinny class has a static method to move 
    # multiple spinnys, without using gyro drive
    spinny.spin_multi_motors([front_lift,rear_lift])    


    #gyro_drive('d', 50, -30, spinny_list= [front_lift, rear_lift] )

    exit(0) # this is fun. It causes your code to crash at the end
            # so you do not have to press the stop button
            # it will throw an error but who cares
'''

## Presentations:<br/>
   [Spike Python Knowledge Base](https://spike.legoeducation.com/prime/help/lls-help-python#lls-help-python) Get started learning Micro Python on the Spike Hub.

   [2025 Gyro Drive - Getting Ready and Testing](https://docs.google.com/presentation/d/1amNZU9LRctaRJAooBi0PKXYJnOBhwPlg/edit?usp=drive_link&ouid=101907280092550552910&rtpof=true&sd=true) This presentation is designed as a teaser to show the 2025 Gyro Drive in action. 
   
   [2025 Gyro Drive - Introduction](https://docs.google.com/presentation/d/188H9rtgRhQCyudcpyrNF0xblFkjz2TN0/edit?usp=drive_link&ouid=101907280092550552910&rtpof=true&sd=true) Adapted to Spike Prime using MicroPython in 2025, this solution does not use native Spike HUB distance calculations, acceleration, or angle navigation. Instead, it reads the sensors, does the math and applies power to the motors. The math is elementary (line number and averages) enough for our FLL Challenge target audience.  

   [2025 Gyro Drive - Installation](https://docs.google.com/presentation/d/1StXtoenVKDPdTLVKF6ZPAseEpUJxdh-d/edit?usp=sharing&ouid=101907280092550552910&rtpof=true&sd=true) This presentation assumes you are familiar with this code. Before setting up your robot, you should read through all the  2025 Gyro Drive presentations so you are familiar with the terms and code layout. 

   [2025 Gyro Drive - Functions and CLasses](https://docs.google.com/presentation/d/1N44QiTRXHaxvKKckrZj5UqavOmP87Bcg/edit?usp=drive_link&ouid=101907280092550552910&rtpof=true&sd=true) Gyro Drive contains a set of functions and classes, used in concert with Spike MicroPython, to support accurate navigation on the Spike Hub. Allow any FLL team to navigate, with great accuracy, any season’s Challenge field while waving to their moms.
   
   [2025 Gyro Drive - The Explainer](https://docs.google.com/presentation/d/1dotNzD7d5yuKdkYch2Xy5eUoNf2iQtjbXXFpTek9EIk/edit?usp=sharing) This presentation explaines how the various concepts like naviagation  work. This can be used to get you team members conversant with the concepts. Suggest you tackle this later in the season.

   [2025 Gyro Drive - Spinny Class](https://docs.google.com/presentation/d/17xijn_pu9CCdgxX3U1fAiIENyofOKOVt/edit?usp=sharing&ouid=101907280092550552910&rtpof=true&sd=true) The Spinny class is an instance that allows you to run a motor to support an arm, lifter, or other spinny attachment. We used a class because it can be instantiated any number of times to support different spinny purposes. 


## Videos:<br/>
   [2025 Gyro Drive Spike Python - Getting Ready and Testing](https://youtu.be/Nl_ngaE-1OA) This is a taste of the 2025 Gyro Drive Spike Python Tool Kit. Please do the homework so you can be ready. This will show you working code examples we use the validate the robot settings.
   
   [2025 Gyro Drive Spike Python - Walking The Code](https://youtu.be/R-VimpPF5ug) This video will demonstrate a few programs. We will walk the code with you so you can see the robot moving and the code making moves.

## Versions:<br/>
   spp 25-06-13.llsb - This is a beta release. This code has been fully tested and works as expected. This is a Spike Python code file not a text file. 

