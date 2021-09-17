---
layout: page
title: fault diagnosis
description: from deterministic to probabilistic
img:
importance: 1
category: research topics
---

<u>Joint work with</u>: xx, yy, zz.

<u>Summary</u>: one/two sentences. Link to [why this is important](#top) and what is the [state of the art](#state-of-the-art) of the research on it, [how we are contributing](#our-contribution) to the problem and what [challenges we are looking to](#open-problems) for the future.

## Motivation

* General motivation on making systems safe and reliable. Just making them work is not enough for critical systems such as
   - transportation (cars, trains, airplanes, ...)
   - fundamental infrastructures such as power grid, road networks, communication networks, ...
   - industrial processes with high stored energy such as nuclear, chemical, steelmaking, etc ...
   - autonomous robots (we are not supposed to send in a human or a second robot to repair the first one, ain't we?)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/1_fault_diagnosis/airbus.jpg' | relative_url }}" alt="" title="Airbus airplane"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/1_fault_diagnosis/pernis.jpg' | relative_url }}" alt="" title="Pernis refinery"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/1_fault_diagnosis/Perseverance.jpg' | relative_url }}" alt="" title="Perseverance autonomous planetary rover on Mars"/>
    </div>
</div>
<div class="caption">
    Examples of systems where fault tolerance is a required property. On the left, an Airbus A321 jet liner. Middle, the Pernis refinery operated by Shell in Rotterdam. Right, the Perseverance autonomous planetary rover on Mars.
</div>

<!-- NOTE: find a better alignment, or choose a middle image with same height as the others, or fit a second row of images only in the left and right columns -->

* While avoiding catastrophic failures in one of the examples above is of paramount importance, on the long run also smaller faults and breakdowns should be minimized. Let us take, for example, the xx sector and look at its Operation&Maintenance cost, which is part of the so called Opex cost, that is the amount of money that must be spent on top of the Capex (the cost of actually making and installing it). Well, there the O&M can be up to yy % of the total (reference to the source). So, every cent that we can save by better diagnosing the onset of faults and thus optimizing maintenance, is a cent that helps reducing the total cost of energy produced by a xx, thus making renewable energy even more sustainable (ref. to another source).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/fault_tolerance.png' | relative_url }}" alt="" title="Fault tolerance concept"/>
    </div>
</div>
<div class="caption">
    On the left, the path leading to a failure. On the right, the one leading to reliability and safety, even in the presence of faults.
</div>

## State of the art

* Fault diagnosis is essentially a classification problem. You want to classify the behaviour of a given system as either healthy or faulty (this first step is called detection). Of course, you may also want to classify which of the possible faulty behaviour is occurring (isolation), and how severe is the fault (estimation). All this information together can be used by the supervisory control system to decide how to cope with the fault (safe stop? Reconfigure the plant and continue to operate, possibly with reduced performances?)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/brake_system_malfunction.jpg' | relative_url }}" alt="" title="Brake system malfunction"/>
    </div>
</div>
<div class="caption">
    The kind of message you would never want to see on your car's dashboard. Not a great example of being fault tolerant, but hey this fault was detected!
</div>

<!-- NOTE: remove all the black around the figure -->


* The way to answer this question, is to introduce two metrics that quantify how good a threshold is. The first one is the *True Positive Rate* ($$\textrm{TPR} = \frac{\textrm{TP}}{\textrm{P}}$$, explain), the other is a *False Positive Rate* ($$\textrm{FPR} = \frac{\textrm{FP}}{\textrm{N}}$$, explain)
    * possibly use images of cats and other stuff, with some possible correct and wrong answers.
    * note, it holds $$\textrm{FPR} = 1 - \textrm{TNR}$$ where TNR is the *True Negative Rate*. Sometimes, especially in the Systems & Control community, we use also the *Missed Detection Rate* MDR, which is the same as the *False Negative Rate* $$\textrm{MDR} = \textrm{FNR} = 1 - \textrm{TPR}$$

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/cat_detector.jpg' | relative_url }}" alt="" title="Brake system malfunction"/>
    </div>
</div>
<div class="caption">
    Let us replace the word "fault" in "fault detector" with "cat". The classification problem now corresponds to detecting whether we do not have a cat (which means everything is fine) and having one (disclaimer: I love cats, but please just look at the evil eyes of <i>these</i> cats). As the cat detector is a binary classifier, we have the four possible scenarios depicted here. Two corresponds to correct classification (true negative and true positive), two to wrong ones (false positive and false negative).
</div>

<!-- NOTE: edited the _base.scss style such that the word b>Figure:</b> is added automatically (make a new class for this) -->

* First of all, no perfect classifier exists (if you wondered why Google as well cannot exactly classify correctly 100% of images containing cats or other flurry pets, this is the reason.) So we need to decide whether we can live with some false positives, some false negatives or a combination thereof. What is best anyway?
 
* Possibly introduce picture of a [ROC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) curve for the cat detector, with entertaining comments on possible behaviours (the flip the coin detector, the good one, the one flipping answers on purpose because it was coded by a dog, the one always saying "cat" and the one always saying "no cat"). Funny thing, the always "no cat" detector can fool us in thinking that it is 100% accurate if we only show it pictures without cats, the same reasoning goes for the always "cat". So be suspicious when somebody gives you a classifier with 100% accuracy.
* A ROC is obtained by letting some parameter of the detector vary in its allowed range. In most case this parameter is the so-called *threshold* (more on that shortly).
    * Some epistemological consideration on faults being luckily rare (Black swan hiding here), so we have not a lot of data about them, or first-principle knowledge for all of them. Instead, data or models about normal healthy behaviour is relatively abundant. So it is quite a solid reasoning to opt for minimizing or reducing to zero the false positives. And then be content with whatever false negatives we come up with.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/ROC_curve.png' | relative_url }}" alt="" title="Brake system malfunction"/>
    </div>
</div>
<div class="caption">
    Let us assume our cat detector is parameterized and that, for each possible value of this parameter, we compute the FPR and TPR over a given set of inputs to be classified. By doing this we can plot a trace, which is called the <i>Receiver Operating Characteristic</i> (ROC), where each point with coordinates (FPR,TPR) is obtained for one value of the parameter. Different detectors will correspond to different kind of curves in this plane. Some notable kinds are: the "flipping the coin" detectors, which randomly decides over the two possible decisions (actually they may be described by any point on the orange line, which one depends on the cat/not cat ratio of samples in the set being classified); good and better detectors, which are above the "flipping the coin" line; the "perfect detector", which is the idealized case to which increasingly better detectors will tend (here, everything is classified correctly, so we have only the (0,1) point); then three possible kind of very bad detectors, such as the "always cat" which will just say "cat" and corresponds to (1,1); the "always not cat" which corresponds to (0,0); the "perfectly malicious detector" which just says the opposite of the perfect detector, and has probably been coded by an evil cat to misguide us. Note: if we had a set of inputs containing only cats, the "always cat" detector may wrongly appear to us a perfect detector. Similarly, the "always not cat" would fool us in thinking it is perfect when presented only with non cat inputs. While this may seem obvious, this has important practical implications as most of the time a fault detector will be presented with non-faulty inputs.
</div>

<!-- NOTE: move most of the discussion from this caption to main text. -->

* In order to do this, we need a way to describe what is the system's healthy behaviour.
  * We use the model-based approach, it is more demanding on the user side (as we need knowledge about a model) but it gives nice theoretical guarantees. Anyway, signal-based approaches, which require just knowledge of how a healthy signal from a system looks like, are very popular in the industrial practice.
  * In the model based ... include figures here from my slide

<!-- <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/model_based.png' | relative_url }}" alt="" title="Model based fault detection"/>
    </div>
</div> -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/1_fault_diagnosis/observer_residual_generation.png' | relative_url }}" alt="" title="Brake system malfunction"/>
    </div>
</div>
<div class="caption">
    Top: the general structure of a model-based fault detection scheme, where a mathematical model is used to generate the so-called <i>residual</i> and <i>threshold</i>. The residual is then tested against the threshold in order to generate an alarm.
    Bottom: a possible mechanism for generating a residual using an observer for a dynamical system.
</div>

  * The key point is generating a residual and a threshold. The residual describes the difference between the theoretical healthy behaviour, and the actual one measured via the sensors. The threshold is a way to decide when to classify the residual as healthy (or physiological as a MD would say), or faulty (pathological). The reason for requiring a threshold is that uncertainties in the model used, and noise in the sensors cause the residual to be non-zero also in healthy condition. The threshold quantify how much we know the effect of these non-idealities can be.
  * And here comes the central problem in fault diagnosis. How to choose an optimal threshold? (note for self: talk about geometric methods first and in a nice way, then complain about non-rigorous papers) (footnote: interestingly, or worryingly enough, a lot of papers on fault diagnosis omit to explicitly define a threshold, leaving this choice to the user. Some other papers assume that a perfect residual can be generated that is sensitive only to faults and not to uncertainties, such that the threshold can be set to zero. These works make geometrical assumptions, basically faults and uncertainties are assumed to act in an orthogonal way with respect to each other, and can be applied to linear systems and some nonlinear one (cite De Persis). The question here is: how robust are these to the fact that our knowledge of the system model is itself uncertain, and that anyway system dynamics can change over time due to environmental and operating conditions, and normal wear?)

[back to top](#top)

## Our contribution

* How using a deterministic threshold designed in order to guarantee 0% false positives is going to have an impractically high false negative rate. So operators will not be bothered by false alarms and trust the system, except for the fact that when a fault occurs the system will most likely not give an alarm and this can lead to serious consequences.
* The issue is that a deterministic threshold such this must be robust even to really large, albeit really rare values of the uncertainties (the ones in the model, and in the measurements).
* It makes much more sense, in practice, to tolerate that in some rare case we get a false alarm, but in return false negatives are back to some useful value and catastrophes are avoided. In any case, better to err on the safe side, isn't it? A false positive is a nuisance but will not let an impending failure being undetected.
* How did we contribute?
  * Initially I continued working with deterministic thresholds, but extended the problem formulation to large scale systems. They are systems too large for a centralized implementation of the fault diagnosis algorithm, as it will require updating in real time a model too complex (limited computational power at a single node), and also feed it too many measurements (limited bandwidth). Furthermore a centralized FDI is not robust per se. Our idea was simple and classic: divide et impera. The model was decomposed and the task split amongst several nodes (cite my 2012 TAC paper). In 2015 then we investigated how to come up to an optimal decomposition, that will respect available computational and communication constraints at each node and optimize overall detectability capabilities.
  * Then we moved (things with Vahab, cite ACC paper and the last TAC with him as well)
    * here we can have figures from the thresholds, our sausages, and formal definitions of probabilistic robust threshold, and the optimization problem we formulated
    * some plots with numerical results from ACC
  * Link to other probabilistic work in <a href=" {{ "projects/research_topics/5_active_inference" | relative_url }}">active inference</a>
 * [back to top](#top)


## Open problems

* Some more meaningful definition of performances for FDI, which include the effects of a false positive/negative. I.e. being able to detect a lot of unconsequential faults but missing almost always catastrophic ones should be properly accounted for via a risk-based metric.
* Uncertainty propagation in nonlinear dynamical systems. We desperately need this to design probabilistically robust thresholds for realistic cases (reality is far from being linear).
* The following methods are promising, but all comes with limitations
  * a
  * b
  * c
* We need some general method that scales well (i.e. not exponentially) and can be implemented numerically in an efficient way.
 * [back to top](#top)

I need to write something here.