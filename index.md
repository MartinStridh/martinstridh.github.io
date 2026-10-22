## Welcome to the Community!
The Lund ECG Parser Research Community is an open research community dedicated to developing and applying the Lund ECG Parser software (formerly commercialized under the names Cardiolund ECG Parser and Cardiolund AFR Tracker) in ECG-related research and development.

## About the Lund ECG Parser and Lund AFR Tracker

### Lund ECG Parser
The Lund ECG Parser is an automated software tool that transforms 1-lead to 12-lead electrocardiogram (ECG) signals (ranging from 10 seconds to weeks in duration) into detailed, machine-readable descriptions. Instead of acting purely as a diagnostic tool, it extracts metadata, performs beat detection and classification, measures intervals (such as heart rate, QTc, and RR variability), and categorizes signals into distinct clinical groups for use in AI, statistical analysis, and database filtering.

The Lund ECG Parser has been integrated into several commercial cardiac monitoring systems, clinical screening trials, and research datasets for automated ECG rhythm analysis and atrial fibrillation (AF) detection:

#### Core Functions
> • ECG Diagnostics/Phenotyping: Analyzes waveforms to detect heartbeats, classify normal or ectopic beats (SVES/VES), measure advanced intervals (HR, QTc, RR), and isolate P-waves for atrial activity tracking.
>
> • Machine Annotation: Generates structured, machine-readable metadata with precise timestamps of arrhythmic events.
>
> • Database Content Analysis: Optimizes large-scale data mining in big patient databases, enabling custom algorithmic searches and providing rich metadata to train or validate AI and clinical decision models.
>
> • Patient Categorisation: Streamlines clinical workflows by automatically sorting and categorizing ECG segments or full recordings to optimize patient management.

#### Previous Commercial & Medical Device Integrations
The software has been integrated into several commercial systems including Zenicor's handheld thumb-ECG systems for remote cardiology diagnostics and stroke prevention to perform interval measurements, beat classification, and rhythm categorization, and PulseOn’s data management service to support wrist-worn ECG devices for outpatient atrial fibrillation detection.

#### Clinical Studies & Research Programs
>• STROKESTOP Studies: Validated in landmark Swedish population screening studies for detecting atrial fibrillation.
>
>• SAFER Study / SAFER Feasibility Study: Used for quality labeling and rhythm identification in the SAFER screening program (Screening for Atrial Fibrillation with ECG to Reduce Stroke) using Zenicor thumb-ECG devices.
>
>• General Clinical & AI Research: Employed by researchers and healthcare databases to generate machine-readable metadata, perform automated signal categorization into 13 categories, and reduce manual ECG review workloads.

<br>

### Lund AFR Tracker

The Lund AFR Tracker is a specialized ECG analysis software extension to Lund ECG Parser that automatically calculates the Atrial Fibrillatory Rate (AFR) from ECG signals.

#### Core Function
> • It measures the repetition rate and the degree of organization of atrial fibrillatory waves (f-waves) in the ECG.
>
> • Technical Process: It removes ventricular activity (QRS complexes and T-waves) via spatiotemporal QRST cancellation and applies sequential time-frequency tracking.
>
> • Resolution & Output: It analyzes signals on a second-to-second basis, generating trends, segment-wise averages, and standard deviations over minutes, hours, or multi-day Holter recordings.
> 
> • Requirements: It is designed for 12-lead ECG systems (most commonly using lead V1) or specialized Holter/esophagus/veterinary leads with a strong atrial signal.

#### Where Has It Been Used?
The Lund AFR Tracker has been used extensively in cardiology research to study atrial electrical properties and predict the outcomes of direct current (DC) cardioversion, ablation therapy, and spontaneous termination of paroxysmal atrial fibrillation (AF). It has been applied to extract f-wave/AFR data from implantable loop recorders (ILRs) and cardiac monitors to evaluate long-term AF burden and remodeling. It is also validated and utilized in large-animal (equine) clinical studies to monitor atrial fibrillatory dynamics and post-cardioversion recurrence in horses with persistent AF.

#### Use in Antiarrhythmic Drug Response Studies
> • Drug Action Monitoring: The AFR Tracker measures how fast or slow the atrial activation rate becomes following pharmacological intervention, acting as a non-invasive surrogate marker for changes in the atrial action potential duration and effective refractory period.
> 
> • Specific Drug Studies: It has been used to track and quantify atrial rate slowing and prediction of drug-induced conversion for established and novel antiarrhythmic agents—including flecainide, dofetilide, ranolazine, quinidine, AZD7009, SECRET and SECRET.
>
> • Predicting Success: A lower or dropping AFR during drug therapy generally indicates a higher likelihood of successful pharmacological or electrical cardioversion, whereas a high or unreduced AFR often correlates with drug resistance or early recurrence.

<br>

## How to use Lund ECG Parser and Lund AFR Tracker?

For more information, please contact:   
Martin Stridh (martin.stridh@bme.lth.se) 

_Principal Investigator and Project Leader_


<!-- Den globala hamburgerknappen för alla skärmar -->
<button class="fixed-hamburger-btn" id="triggerMobileMenu">☰ Menu</button>

<!-- Den fristående sidopanelen med alla dina 8 unika länkar -->
<div id="clean-mobile-drawer" class="custom-mobile-drawer">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/page1.html">Join the community</a></li>
    <li><a href="/page2.html">Lund ECG Parser explained</a></li>
    <li><a href="/page2.html">Lund AFR Tracker explained</a></li>
    <li><a href="/page2.html">Package description</a></li>
    <li><a href="/page2.html">Downloads</a></li>
    <li><a href="/page2.html">Documentation</a></li>
    <li><a href="/page2.html">Publications</a></li>
  </ul>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    var btn = document.getElementById("triggerMobileMenu");
    var drawer = document.getElementById("clean-mobile-drawer");

    if (btn && drawer) {
      // Öppna och stäng stabilt vid tryck/klick
      btn.addEventListener("click", function(e) {
        e.stopPropagation();
        drawer.classList.toggle("drawer-is-open");
      });

      // Stäng menyn om man klickar på texten utanför sidopanelen
      document.addEventListener("click", function(e) {
        if (drawer.classList.contains("drawer-is-open")) {
          if (!drawer.contains(e.target) && e.target !== btn) {
            drawer.classList.remove("drawer-is-open");
          }
        }
      });
    }
  });
</script>
