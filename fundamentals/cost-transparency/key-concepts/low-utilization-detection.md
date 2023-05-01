# Low Utilization Detection

This feature identifies underutilized EC2, RDS and ECS resources and recommends cost-saving actions such as rightsizing or instance shut-off (for stone-cold resources).

Underutilized EC2 instances are definitely among the most common obstacles on the way to cloud compute cost efficiency in AWS. Your engineering teams are launching instances at scale, and not all of those instances are sized properly. As a result, money gets wasted and wrong commitments are made.

Cloudthread platform now uncovers underutilized EC2 instances for you and recommends better fitting instance sizes. Utilization is measured for CPU and Memory dimensions, and resources with less than a customizable threshold get surfaced with an appropriate resizing recommendation. Potential savings get calculated and highlighted as well, so that you know what should be adjusted first.\
