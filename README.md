# ft_test

```
#include <pthread.h>

void setup_realtime_scheduling() {
    struct sched_param param;
    param.sched_priority = 99;
    if (sched_setscheduler(0, SCHED_FIFO, &param) != 0) {
        perror("sched_setscheduler failed");
    }
}

int main(int argc, char *argv[]) {
    setup_realtime_scheduling();
}

```
