TelephoneBooth




The problem statement here asks us to develop an interactive software that would demonstrate process synchronization problem using semaphores, busy waiting, spinlocks, monitors, critical section,etc.

We have decided to take up an example of telephone booth and implement above concepts.

A person who wants to make a call would resemble a process. A phone booth, consisting of a single telephone(at least for the time being)would act as a resource. The person entering the telephone booth would resemble a process entering a critical section. Now since the duration of each call may vary, there will be a constant checking from other people(processes) waiting for their turn to make a call(enter the critical section).Now a binary semaphore would be used in this case. Any person entering the booth would call wait() before entering. People waiting for their turn would constantly check this variable. Now as soon as a person has finished his call, signal() would be called and the state of binary semaphore would be altered, indicating a new person can enter the booth.

Now the above problem will become more trivial when number of phones in the booth would be increased. This would require more semaphores to be implemented.
