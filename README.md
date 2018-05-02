# Almost-Increasing-Sequence
Almost Increasing Sequence Solution in C++

bool almostIncreasingSequence(std::vector<int> sequence) {
    int res=0;
    int max= -10000, secondmax= -10000;
    for (int i=0; i<sequence.size(); i++)
    {
       if (sequence[i]>max)
       {
           secondmax=max;
           max= sequence[i];
       }
        else if (sequence[i]>secondmax)
        {
            max= sequence[i];
            res++;
        }
        else res++;
    }
    return (res<2);
}

