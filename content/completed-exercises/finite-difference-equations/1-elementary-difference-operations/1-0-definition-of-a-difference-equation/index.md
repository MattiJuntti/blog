+++
title  = "1.0. Definition of a difference equation"
layout = "solution-single"
+++

<span class = "exnum">1</span> The difference table for sequences

$$
    \begin{array}{r l}
        (\text{i})   & 0, 2,  6, 12,  20,  30,  42, 56, \ldots \\        
        (\text{ii})  & 0, 4, 18, 48, 100, 180, 294,     \ldots \\
        (\text{iii}) & 1, 3, 19, 85, 261, 631,          \ldots \\
    \end{array}
$$

are,

<div style = "text-align: left;
              margin: 16px 0 0 16px;">
\(
    \begin{array}{ r c c c c }
        (\text{i}): &          &               &          &             \\[0.0em]
                  0 &          &               &          &             \\[0.0em]
                    & \searrow &               &          &             \\[0.0em]
                    &          & 2 - 0 = 2     &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                  2 &          &               &          & 4 - 2 = 2   \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 6 - 2 = 4     &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                  6 &          &               &          & 6 - 4 = 2   \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 12 - 6 = 6    &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                 12 &          &               &          & 8 - 6 = 2   \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 20 - 12 = 8   &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                 20 &          &               &          & 10 - 8 = 2  \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 30 - 20 = 10  &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                 30 &          &               &          & 12 - 10 = 2 \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 42 - 30 = 12  &          &             \\[0.0em]
                    & \nearrow &               & \searrow &             \\[0.0em]
                 42 &          &               &          & 14 - 12 = 2 \\[0.0em]
                    & \searrow &               & \nearrow &             \\[0.0em]
                    &          & 56 - 42 = 14  &          &             \\[0.0em]
                    & \nearrow &               &          &             \\[0.0em]
                 56 &          &               &          &             \\[0.0em]
    \end{array}
\)
</div>

<div style = "text-align: left;
              margin: 32px 0 0 16px;">
\(
    \begin{array}{ r c c c c }
       (\text{ii}): &          &                 &          &               &          &             \\[0.0em]
                  0 &          &                 &          &               &          &             \\[0.0em]
                    & \searrow &                 &          &               &          &             \\[0.0em]
                    &          & 4 - 0 = 4       &          &               &          &             \\[0.0em]
                    & \nearrow &                 & \searrow &               &          &             \\[0.0em]
                  4 &          &                 &          & 14 - 4 = 10   &          &             \\[0.0em]
                    & \searrow &                 & \nearrow &               & \searrow &             \\[0.0em]
                    &          & 18 - 4 = 14     &          &               &          & 16 - 10 = 6 \\[0.0em]
                    & \nearrow &                 & \searrow &               & \nearrow &             \\[0.0em]
                 18 &          &                 &          & 30 - 14 = 16  &          &             \\[0.0em]
                    & \searrow &                 & \nearrow &               & \searrow &             \\[0.0em]
                    &          & 48 - 18 = 30    &          &               &          & 22 - 16 = 6 \\[0.0em]
                    & \nearrow &                 & \searrow &               & \nearrow &             \\[0.0em]
                 48 &          &                 &          & 52 - 30 = 22  &          &             \\[0.0em]
                    & \searrow &                 & \nearrow &               & \searrow &             \\[0.0em]
                    &          & 100 - 48 = 52   &          &               &          & 28 - 22 = 6 \\[0.0em]
                    & \nearrow &                 & \searrow &               & \nearrow &             \\[0.0em]
                100 &          &                 &          & 80 - 52 = 28  &          &             \\[0.0em]
                    & \searrow &                 & \nearrow &               & \searrow &             \\[0.0em]
                    &          & 180 - 100 = 80  &          &               &          & 34 - 28 = 6 \\[0.0em]
                    & \nearrow &                 & \searrow &               & \nearrow &             \\[0.0em]
                180 &          &                 &          & 114 - 80 = 34 &          &             \\[0.0em]
                    & \searrow &                 &          &               &          &             \\[0.0em]
                    &          & 294 - 180 = 114 &          &               &          &             \\[0.0em]
                    & \nearrow &                 &          &               &          &             \\[0.0em]
                294 &          &                 &          &               &          &             \\[0.0em]
    \end{array}
\)
</div>

<div style = "text-align: left;
              margin: 32px 0 0 16px;">
\(
    \begin{array}{ r c c c c }
      (\text{iii}): &          &                 &          &                 &          &                 &          &                &          &                \\[0.0em]
                  1 &          &                 &          &                 &          &                 &          &                &          &                \\[0.0em]
                    & \searrow &                 &          &                 &          &                 &          &                &          &                \\[0.0em]
                    &          & 3 - 1 = 3       &          &                 &          &                 &          &                &          &                \\[0.0em]
                    & \nearrow &                 & \searrow &                 &          &                 &          &                &          &                \\[0.0em]
                  3 &          &                 &          & 16 - 3 = 13     &          &                 &          &                &          &                \\[0.0em]
                    & \searrow &                 & \nearrow &                 & \searrow &                 &          &                &          &                \\[0.0em]
                    &          & 19 - 3 = 16     &          &                 &          & 50 - 13 = 37    &          &                &          &                \\[0.0em]
                    & \nearrow &                 & \searrow &                 & \nearrow &                 & \searrow &                &          &                \\[0.0em]
                 19 &          &                 &          & 66 - 16 = 50    &          &                 &          & 50 - 37 = 13   &          &                \\[0.0em]
                    & \searrow &                 & \nearrow &                 & \searrow &                 & \nearrow &                & \searrow &                \\[0.0em]
                    &          & 85 - 19 = 66    &          &                 &          & 110 - 50 = 60   &          &                &          & 189            \\[0.0em]
                    & \nearrow &                 & \searrow &                 & \nearrow &                 & \searrow &                & \nearrow &                \\[0.0em]
                 85 &          &                 &          & 176 - 66 = 110  &          &                 &          & 262 - 60 = 202 &          &                \\[0.0em]
                    & \searrow &                 & \nearrow &                 & \searrow &                 & \nearrow &                &          &                \\[0.0em]
                    &          & 261 - 85 = 176  &          &                 &          & 372 - 110 = 262 &          &                &          &                \\[0.0em]
                    & \nearrow &                 & \searrow &                 & \nearrow &                 &          &                &          &                \\[0.0em]
                261 &          &                 &          & 631 - 261 = 372 &          &                 &          &                &          &                \\[0.0em]
                    & \searrow &                 & \nearrow &                 &          &                 &          &                &          &                \\[0.0em]
                    &          & 631 - 261 = 370 &          &                 &          &                 &          &                &          &                \\[0.0em]
                    & \nearrow &                 &          &                 &          &                 &          &                &          &                \\[0.0em]
                631 &          &                 &          &                 &          &                 &          &                &          &                \\[0.0em]
    \end{array}
\)
</div>

