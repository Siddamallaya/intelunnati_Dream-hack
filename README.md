Due to object detection’s close relationship with
video analysis and image understanding, it has attracted much
research attention in recent years. Traditional object detection
methods are built on handcrafted features and shallow trainable
architectures. Their performance easily stagnates by constructing
complex ensembles which combine multiple low-level image
features with high-level context from object detectors and scene
classifiers. With the rapid development in deep learning, more
powerful tools, which are able to learn semantic, high-level,
deeper features, are introduced to address the problems existing
in traditional architectures. These models behave differently
in network architecture, training strategy and optimization
function, etc. In this paper, we provide a review on deep
learning based object detection frameworks. Our review begins
with a brief introduction on the history of deep learning and
its representative tool, namely Convolutional Neural Network
(CNN). Then we focus on typical generic object detection
architectures along with some modifications and useful tricks
to improve detection performance further. As distinct specific
detection tasks exhibit different characteristics, we also briefly
survey several specific tasks, including salient object detection,
face detection and pedestrian detection. Experimental analyses
are also provided to compare various methods and draw some
meaningful conclusions. Finally, several promising directions and
tasks are provided to serve as guidelines for future work in
both object detection and relevant neural network based learning
systems.

In spite of rapid development and achieved promising
progress of object detection, there are still many open issues
for future work.

The first one is small object detection such as occurring
in COCO dataset and in face detection task. To improve
localization accuracy on small objects under partial occlusions,
it is necessary to modify network architectures from the
following aspects.

• Multi-task joint optimization and multi-modal information fusion. Due to the correlations between different
tasks within and outside object detection, multi-task joint
optimization has already been studied by many researchers
[16] [18]. However, apart from the tasks mentioned in
Subs. III-A8, it is desirable to think over the characteristics
of different sub-tasks of object detection (e.g. superpixel
semantic segmentation in salient object detection) and extend multi-task optimization to other applications such as
instance segmentation [66], multi-object tracking [202] and
multi-person pose estimation [S4]. Besides, given a specific
application, the information from different modalities, such
as text [212], thermal data [205] and images [65], can be
fused together to achieve a more discriminant network.

• Scale adaption. Objects usually exist in different scales,
which is more apparent in face detection and pedestrian
detection. To increase the robustness to scale changes, it
is demanded to train scale-invariant, multi-scale or scaleadaptive detectors. For scale-invariant detectors, more powerful backbone architectures (e.g. ResNext [123]), negative
sample mining [113], reverse connection [213] and subcategory modelling [60] are all beneficial. For multi-scale
detectors, both the FPN [66] which produces multi-scale
feature maps and Generative Adversarial Network [214]
which narrows representation differences between small objects and the large ones with a low-cost architecture provide
insights into generating meaningful feature pyramid. For
scale-adaptive detectors, it is useful to combine knowledge
graph [215], attentional mechanism [216], cascade network
[180] and scale distribution estimation [171] to detect objects adaptively.

• Spatial correlations and contextual modelling. Spatial
distribution plays an important role in object detection. So
region proposal generation and grid regression are taken
to obtain probable object locations. However, the correlations between multiple proposals and object categories
are ignored. Besides, the global structure information is
abandoned by the position-sensitive score maps in R-FCN.
To solve these problems, we can refer to diverse subset
selection [217] and sequential reasoning tasks [218] for
possible solutions. It is also meaningful to mask salient parts
and couple them with the global structure in a joint-learning
manner [219].

The second one is to release the burden on manual labor and
accomplish real-time object detection, with the emergence of
large-scale image and video data. The following three aspects
can be taken into account.

• Cascade network. In a cascade network, a cascade of
detectors are built in different stages or layers [180], [220].
And easily distinguishable examples are rejected at shallow
layers so that features and classifiers at latter stages can
handle more difficult samples with the aid of the decisions
from previous stages. However, current cascades are built in
a greedy manner, where previous stages in cascade are fixed
when training a new stage. So the optimizations of different
CNNs are isolated, which stresses the necessity of end-toend optimization for CNN cascade. At the same time, it
is also a matter of concern to build contextual associated
cascade networks with existing layers.

• Unsupervised and weakly supervised learning. It’s
very time consuming to manually draw large quantities
of bounding boxes. To release this burden, semantic prior
[55], unsupervised object discovery [221], multiple instance
learning [222] and deep neural network prediction [47] can
be integrated to make best use of image-level supervision to
assign object category tags to corresponding object regions
and refine object boundaries. Furthermore, weakly annotations (e.g. center-click annotations [223]) are also helpful
for achieving high-quality detectors with modest annotation
efforts, especially aided by the mobile platform.

• Network optimization. Given specific applications and
platforms, it is significant to make a balance among speed...


  


![Screenshot (24)](https://github.com/Siddamallaya/intelunnati_Dream-hack/assets/139435973/e6b98bcb-c675-4019-b662-d377a9f52325)

![Screenshot (25)](https://github.com/Siddamallaya/intelunnati_Dream-hack/assets/139435973/53b3c09c-e61b-4f79-bff8-fcc99f4075cf)








