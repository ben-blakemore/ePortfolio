# Humanoid Robot Assignments

As mentioned in my UML page, I feel that these assignments are what I got the most out of in the module. I thought that the problem environment was an interesting one and lent itself well to an object orientated approach. Below are some of my reflections looking back on the system design and implementation assignments.

## System Design
I found that the formative activities in the weeks leading up to the design assignment really helped in understanding the context of the task. I found the reading of chapter 18 in 'Think Python' in Unit 5 especially useful as it helped remind me of some of Python's quirks, such as list comprehension. The section that turned out to be most useful was that on 'unittest', a python package designed to make writing unit tests simpler. A unit test independently verifies the smallest logical component of a program. In procedural or functional programming languages, this is typically a subroutine or function (https://learning.oreilly.com/library/view/python-continuous-integration/9781484242810/html/456760_1_En_1_Chapter.xhtml).

Through previous professional experience, I have used unit tests, but not with Python. Therefore I was interested to read about this package and how it can aid the developer in testing their software. I immediately knew that I would want to make use of this tool when the implementation stage came. I thought that the ability to define separate tests, have them all automatically run and to be presented with a clear output of any failing tests was impressive. I made a note of this and returned to it during the implementation stage.

I took the opportunity to complete the Unit 5 polymorphism exercise and created a simple implementation of Humanoid Robot classes, shown below.

```python
# Base class
class HumanoidRobot:
    def __init__(self, name, model):
        self.name = name
        self.model = model

    def info(self):
        raise NotImplementedError("Subclasses must implement the info method")

    def perform_task(self):
        raise NotImplementedError("Subclasses must implement the perform_task method")

# Subclass 1
class AssemblerRobot(HumanoidRobot):
    def info(self):
        print(f"I am an Assembler Robot. My name is {self.name}, model {self.model}.")

    def perform_task(self):
        print("I help assemble components.")

# Subclass 2
class TransportRobot(HumanoidRobot):
    def info(self):
        print(f"I am a Transport Robot. My name is {self.name}, model {self.model}.")

    def perform_task(self):
        print("I help transport components.")

# Subclass 3
class QualityAssuranceRobot(HumanoidRobot):
    def info(self):
        print(f"I am a Quality Assurance Robot. My name is {self.name}, model {self.model}.")

    def perform_task(self):
        print("I ensure assembled components are of the required standard.")

# Create instances
robot1 = AssemblerRobot("Assembler", "A100")
robot2 = TransportRobot("Transporter", "T300")
robot3 = QualityAssuranceRobot("QualityAssurance", "QA200")

# Use polymorphism
for robot in (robot1, robot2, robot3):
    robot.perform_task()
    robot.info()
    robot.perform_task()
```

My final implementation featured a very similar approach to the handling of tasks, with a parent task class featuring an abstract "execute task" method which was then extended from in subclasses. Completing this exercise proved useful and helped guide the final approach so I feel that it was worthwhile.

On reflection, I found that the reading leading up to the assignment did not present me with much difficulty, as many of the concepts are ones I have been using now for many years in my job. It did however give me time for pause and a chance to think deeper about how best to apply what I already know. I am fortunate enough to approach these tasks with many previous experiences that have helped shape my approach to future similar tasks. For example the separation of logic between the robot, backend and user interface came intuitively to me. Whereas I feel that with less experience this would have been an area of confusion for me.

Overall I feel that the design stage of the assignment went well. The proposed system did not deviate significantly from the end product, which reflects the thorough planning and consideration that went into the design stage. I feel that an area of improvement for me in my job is to sometimes slow down and try and consider the bigger picture. I have always found this a difficult task as it inherently relies on the ability to foresee potential future problems. This design activity has proven to me that taking time before starting to write code can help achieve this, by uncovering potential issues rather than encountering them later in development.
