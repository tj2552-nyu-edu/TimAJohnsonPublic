##From Governance to Enforcement: Closing AI Data Accountability with SLSA
Timothy Johnson, Tandon Cyber Fellow
tj2552@nyu.edu,
NYU AI Governance, Fall 2026, Alexander Sharpe


Current AI governance and risk frameworks generally identify data as the principal agent of AI
performance  and  risk.  But  the  current  recognized  standards,  such  as  ISO  42001,  rely  on  policy,
audit,  documentation,  and  human  oversight  to  secure  downstream  data  pipelines[4].  Although
there is emphasis on data quality and accountability[5], current standards stop short of requiring
data signing and the enforceable assurances it provides. Use of PKI based cryptography ensures
data  is  correct  and  unaltered  and  permanently  attaches  training  artifacts  to  a  human  overseer
signer  utilizing  their  own  private  keys  issued  for  the  exclusive  purpose  of  managing  AI  data.
These  secured  relationships  will  persist  downstream  into  the  model.  Future  input  handling  and
data processing for outputs will benefit from traceability to the source with a verifiable chain of
custody.  This  approach  is  effective  against  recent  documented  AI  failures  caused  by  attackers
poisoning  downstream  training  data,  an  increasing  trend  and  security  risk  [7].  As  AI  systems
become  more  prominent  and  scale  to  projected  future  utilization,  the  reliance  on  policy,  rather
than  technology,  will  become  increasingly  ineffective  and  unsustainable  leading  to  increasingly
poorer  outcomes[6].  This  paper  proposes  supply  chain  security  levels  such  as  those  used  by
product  security  professionals  for  downstream  pre-build  application  security  as  a  technical
prescription  for  this  problem.  Specifically  we  will  explore  Google’s  Supply  Chain  Levels  for
Software  Artifacts  (SLSA)  framework  and  how  it  addresses  ISO  42001’s,  albeit  by  design,
technical  shortcomings.  Although  that  language  is  as  harsh  as  it  is  deliberate,  our  theme  is
enhancement, not replacement.
The  principal  technical  hypocrisy  of  modern AI  frameworks  is  their  emphasis  on  trust  without
enforcing  it.  The  basis  for  all  modern  data  security  is  that  data  cannot  be  secured  until  both
parties  prove  their  identity  and  agree  on  a  security  standard.  Both  of  these  goals  are  achieved
through trusted digital signing with root accountability. SLSA treats all data as security objects. A
chain of certificates would document the entire history of the artifact (training data) how it was
produced, from which inputs and on which verifiable system [1]. By combining these objects and
histories  while  permanently  binding  them  to  a  human  operator,  and  improves  downstream
security  and  accountability.    Instead  of  a  documented  history,  each  data  artifact  will  be  PKI
signed  by  its  originator  and  downstream  processors[2].  This  would  provide  assurances  that  the
data is authentic and unaltered as well as who used it and for what purposes[1].
Modern  AI  frameworks  dictate  documentation,  audit,  and  monitoring  as  key  to  detecting  AI
malfunctions   and   subsequently   correcting   them.   SLSA’s   approach   focuses   on   preventive
assurances.  Recent  research  shows  that  large  language  models  can  be  corrupted  with  as  few  as
250 malicious training documents regardless of dataset size, highlighting a practical vulnerability
in model training that arises from the lack of verifiable data integrity and provenance in existing
AI pipelines. Secure supply chain approaches, championed by product security practitioners, and
if  used  properly,  mitigates  this  risk.  The  artifact  (training  data  object(s))  can  not  proceed

downstream without ownership approval, verification, and approval all signed cryptographically
[2].  This  is  a  matter  of  technological  automation  and  workflows,  not  merely  documentation.
Such  a  digital  history  simplifies  retroactive  audit.  Since  digital  signing  requires  hashing,  the
process would make data tampering virtually impossible.
It is generally recommended best-practice to build AI systems in isolated sandboxes. This is not
an  explicit  ISO42001  control  in  and  of  itself  though  implied.  SLSA  explicitly  prescribes  that
approach as a matter of trust. Existing frameworks focus on access controls, separation of duties,
accountability and other IAM central controls but presume these work as expected or depend on
retro  audit  to  discover  and  correct  deficiencies.  If  AI  development  and  adoption  grows  as
projected due to demand, and automated pipelines become consequently more complex, existing
controls  will  grow  weaker.  By  confining  build  processes  and  data  artifacts  into  isolated,  secure
micro environments [2][3], control are more effective, easier to implement, and outcomes more
predictable.  This  ensures  data  comes  from  and  processed  by  trusted  systems  and  actors  while
reducing the risk of compromise.
Upstream data security with signing solves trust, integrity, and accountability failures at the point
where  AI  behavior  is  determined  and  data  breaches  are  likely  to  occur.  By  enhancing,  not
replacing,  ISO42001  with  the  SLSA  standard,  these  problems  are  technically  treated  and
cryptographically  addressed.  SLSA  helps  add  enforcement  to  areas  ISO42001  highlights  as
crucial to safe AI development and operation. Brian Christian’s The Alignment Problem predicts
the  accelerated  nature  of  technology  adoption  and  delayed  effective  governance  policies  and
keeping  those  policies  up  to  date[6].  AI  is  arguably  the  fastest  growing  technology  segment
today  and  is  likely  to  remain  so  for  the  foreseeable  future.  SLSA  addresses  this  challenge  by
prescribing  how  to  build  the  automated  downstream  approaches  to  data  security  during  the
model lifecycle that will be needed as development methods evolve to meet demand.
## References
[1] Supply-chain Levels for Software Artifacts, “SLSA Provenance Specification,” slsa.dev.
[2] Supply-chain Levels for Software Artifacts, “SLSA Levels Specification,” slsa.dev.
[3] Supply-chain Levels for Software Artifacts, “SLSA Threat Model,” slsa.dev.
[4]   ISO/IEC,   ISO/IEC   42001:2023   —   Artificial   Intelligence   —   Management   System,
International Organization for Standardization, Geneva, Switzerland, 2023.
[5]ISO/IEC, ISO/IEC 42001:2023 — Artificial Intelligence — Management System, Annex A,
Control A.7 (Data for AI Systems). Geneva, Switzerland: International Organization for
[6] B. Christian, The Alignment Problem: Machine Learning and Human Values, New York, NY,
USA: W. W. Norton & Company, 2020.
[7] A. Souly et al., “Poisoning Attacks on LLMs Require a Near-Constant Number of Poison
Samples,” arXiv preprint, Oct. 8, 2025.
