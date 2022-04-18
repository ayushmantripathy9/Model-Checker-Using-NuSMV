On running the code you would see that of the Four Specifications the one specifying transition from 'idle' to 'entering' is FALSE.
This is because the transition idle -> idle exists and the process may starve and never enter Critical Section.

On changing the transition state = critical : {exiting} to state = critical : {critical, exiting} two more specifications become FALSE.
This is because the process on entering the critical section may now choose to stay forever in the Critical Section and never exit the same.