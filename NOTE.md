
2 因为系统的随机性,各步骤的运行顺序是不确定的.
Tracking线程不产生关键帧时,LocalMapping和LoopClosing线程基本上处于空转的状态. 而Tracking线程产生关键帧的频率和时机不是固定的,因此需要3个线程同时运行,LocalMapping和LoopClosing线程不断循环查询Tracking线程是否产生关键帧,产生了的话就处理.