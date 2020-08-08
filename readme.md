#### Required Tools

- Visual Studio Code
- Docker
- Docker Compose
- AWS Account
- AWS CLI
- Azure Account
- Azure CLI
- Google Cloud Account
- Terraform
- Ansible

## Next Steps

## Diagrams

```

graph architecture {

node[style=filled,color="#59C8DE"]
//node [style=filled,color="#D14D28", fontcolor=white];
rankdir = LR
node[shape=record, width=1.6]


ParentNode1 -- ChildNode1
ChildNode1 -- ChildNode2
ChildNode1 -- ChildNode3
ChildNode1 -- ChildNode4

ParentNode1[label=<Configuration <BR/>and Scripts>]
ChildNode1[label=<Ansible>];
ChildNode2[label=<Server 1>];
ChildNode3[label=<Server 2>];
ChildNode4[label=<Server 3>];

}

graph architecture {
layout="circo";
node[style=filled,  fillcolor="#D14D28", fontcolor=white]
//node [style=filled,color="#D14D28", fontcolor=white];
rankdir = LR
node[shape = circle,  width=1]
edge [dir=forward]

Node1 -- Node2
Node2 -- Node3
Node3 -- Node4
Node4 -- Node1
//Node4 -- Node5
//Node5 -- Node6

Node1[label=<DEV>]
Node2[label=<QA>]
Node3[label=<STAGE>]
Node4[label=<PROD>]
//Node5[label=<5>]
//Node6[label=<6>]

}


graph architecture {
rankdir = LR
node[shape = circle,  width=1, style=filled,fillcolor="#59C8DE"]
//shape = record
edge [dir=forward]

Node1 -- Node2
Node2 -- Node3
Node3 -- Node4
//Node4 -- Node1
//Node4 -- Node5
//Node5 -- Node6

Node1[label=<DEV>]
Node2[label=<QA>]
Node3[label=<STAGE>]
Node4[label=<PROD>]
//Node5[label=<5>]
//Node6[label=<6>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1, style=filled,fillcolor="#59C8DE"]
//shape = record
edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node5 -- Node6
Node6 -- Node7
Node7 -- Node1
Node1 -- Node2
Node2 -- Node3

Node1[label=<Code>]
Node2[label=<Build>]
Node3[label=<Test>]
Node4[label=<Release>]
Node5[label=<Deploy>]
Node6[label=<Review>]
Node7[label=<Plan>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1.3, style=filled,color="#59C8DE", fontcolor=black]
//shape = record
//fillcolor="#59C8DE"
//edge [dir=forward]
edge [width=0]
#D14D28

Node3 -- Node4[style=invis]
Node4 -- Node5[style=invis]
Node1 -- Node2[style=invis]
Node2 -- Node3[style=invis]

Node1[label=<Business>]
Node2[label=<Architecture>]
Node3[label=<Development>]
Node4[label=<Testing>]
Node5[label=<Operations>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1, style=filled,color="#D14D28", fontcolor=white]
//shape = record
//fillcolor="#59C8DE"
edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node5 -- Node6
Node1 -- Node2
Node2 -- Node3

Node1[label=<Vision>]
Node2[label=<Iteration 1>]
Node3[label=<Iteration 2>]
Node4[label=<...>]
Node5[label=<Iteration n>]
Node6[label=<Product>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1, style=filled,fillcolor="#59C8DE"]
//shape = record
edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node5 -- Node6
Node6 -- Node7
Node7 -- Node8
Node8 -- Node1
Node1 -- Node2
Node2 -- Node3

Node1[label=<Code>]
Node2[label=<Build>]
Node3[label=<Test>]
Node4[label=<Release>]
Node5[label=<Deploy>]
Node6[label=<Operate>]
Node7[label=<Monitor>]
Node8[label=<Plan>, fillcolor=white]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=2, style=filled,fillcolor="#D14D28", fontcolor=white]
//shape = record
//edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node5 -- Node6
Node6 -- Node7
Node7 -- Node8
Node8 -- Node1
Node1 -- Node2
Node2 -- Node3

Node1[label=<<FONT POINT-SIZE="20">Continuous<br/>Planning</FONT>>]
Node2[label=<<FONT POINT-SIZE="20">Continuous<br/>Development</FONT>>]
Node3[label=<<FONT POINT-SIZE="20">Continuous<br/>Integration</FONT>>]
Node4[label=<<FONT POINT-SIZE="20">Continuous<br/>Deployment</FONT>>]
Node5[label=<<FONT POINT-SIZE="20">Continuous<br/>Testing</FONT>>]
Node6[label=<<FONT POINT-SIZE="20">Continuous<br/>Delivery</FONT>>]
Node7[label=<<FONT POINT-SIZE="20">Continuous<br/>Monitoring</FONT>>]
Node8[label=<<FONT POINT-SIZE="20">Continuous<br/>Feedback</FONT>>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1.6, style=filled,fillcolor="#D14D28", fontcolor=white]
//shape = record
edge [dir=forward]
{ rank=same Node1 Node2 Node3 }
{ rank=same Node7 Node8 Node9 }

Node3 -- Node4
Node4 -- Node5
Node5 -- Node6
Node6 -- Node7
Node7 -- Node8
Node8 -- Node9
Node1 -- Node2
Node2 -- Node3

Node1[label=<<FONT POINT-SIZE="20">Code<br/>Commit</FONT>>]
Node2[label=<<FONT POINT-SIZE="20">Unit<br/>Tests</FONT>>]
Node3[label=<<FONT POINT-SIZE="20">Integration<br/>Tests</FONT>>]
Node4[label=<<FONT POINT-SIZE="20">Package<br/></FONT>>]
Node5[label=<<FONT POINT-SIZE="20">Deploy</FONT>>]
Node6[label=<<FONT POINT-SIZE="20">Automated<br/> Tests</FONT>>]
Node7[label=<<FONT POINT-SIZE="20">Testing<br/>Approval</FONT>>, fillcolor=white, fontcolor=black]
Node8[label=<<FONT POINT-SIZE="20">Deploy<br/>NEXT</FONT>>]
Node9[label=<<FONT POINT-SIZE="20">..</FONT>>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1.6, style=filled,fillcolor="#D14D28", fontcolor=white]
//shape = record
edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node1 -- Node2
Node2 -- Node3

Node1[label=<<FONT POINT-SIZE="20">Provision<br/>Server</FONT>>]
Node2[label=<<FONT POINT-SIZE="20">Install<br/>Java</FONT>>]
Node3[label=<<FONT POINT-SIZE="20">Install<br/>Tomcat</FONT>>]
Node4[label=<<FONT POINT-SIZE="20">Configure<br/>Tomcat</FONT>>]
Node5[label=<<FONT POINT-SIZE="20">Deploy<br/>Application</FONT>>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1.6, style=filled,fillcolor="#D14D28", fontcolor=white]
//shape = record
edge [dir=forward]

Node3 -- Node4
Node4 -- Node5
Node1 -- Node2
Node2 -- Node3

Node1[label=<<FONT POINT-SIZE="20">Create<br/>Template</FONT>>]
Node2[label=<<FONT POINT-SIZE="20">Provision<br/>Server</FONT>>]
Node3[label=<<FONT POINT-SIZE="20">Install<br/>Software</FONT>>]
Node4[label=<<FONT POINT-SIZE="20">Configure<br/>Software</FONT>>]
Node5[label=<<FONT POINT-SIZE="20">Deploy<br/>App</FONT>>]

}

graph architecture {
rankdir = LR
node[shape = circle,  width=1.6, style=filled,fillcolor="#D14D28", fontcolor=white]
//shape = record
edge [dir=forward]

Node3 -- Node4
Node1 -- Node2
Node2 -- Node3

Node1[label=<<FONT POINT-SIZE="20">Provision<br/>Server v1</FONT>>]
Node2[label=<<FONT POINT-SIZE="20">Provision<br/>Server v2</FONT>>]
Node3[label=<<FONT POINT-SIZE="20">Remove<br/>Server v1</FONT>>]
Node4[label=<<FONT POINT-SIZE="20">..<br/></FONT>>]

}
```

## Todo

- Course Promotion
  - 2 Emails on Udemy
  - 2 Emails to Email List
  - Create YouTube Course Preview Video
    - Add YouTube Course Preview Video as End Video for all videos
    - Make it the YouTube Default Video
  - Release atleast 20 small videos - one a day on Youtube
  - Do atleast 3 Youtube live sessions
  - After a Month
    - UFB
