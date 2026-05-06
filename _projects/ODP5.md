---
layout: project
title: Spotted Lanternfly Trap
description: Client pitch and functional prototype for a vineyard SLF capture system
image: /assets/images/SLF_trap.jpg
---
<style>
.toc-box {
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 1rem 1.25rem;
  margin: 1rem 0 2rem 0;
  background: #000;
}
.toc-box ul {
  margin: 0.5rem 0 0 1.2rem;
}
.section-card {
  margin: 2rem 0 3rem 0;
  padding: 1.25rem;
  border: 1px solid #e5e5e5;
  border-radius: 12px;
  background: black;
}
.pdf-frame {
  width: 100%;
  height: 75vh;
  border: 0;
  margin-top: 1rem;
}
.jump-link {
  text-decoration: none;
  font-weight: 600;
}
.jump-link:hover {
  text-decoration: underline;
}
</style>

## Project Overview
This project proposes and tests a mechanical spotted lanternfly (SLF) trap for vineyard use. The design goal is to trap spotted lanternflies while they feed, using a rotating fan mechanism to sweep them into a one-way trap.

<div class="toc-box">
  <strong>Contents</strong>
  <ul>
    <li><a class="jump-link" href="#client-pitch">Client Pitch</a></li>
    <li><a class="jump-link" href="#functional-prototype">Functional Prototype</a></li>
    <li><a class="jump-link" href="#client-report">Client Report</a></li>
  </ul>
</div>

<div id="client-pitch" class="section-card">
  <h2>Client Pitch</h2>
  <p>
    This milestone presents the original design concept, intended user need, and early validation plan for the spotted lanternfly trap.
  </p>
  <p>
    <a href="{{ '/assets/Client.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open Client.pdf
    </a>
  </p>
  <iframe
    src="{{ '/assets/Client.pdf' | relative_url }}"
    class="pdf-frame"
    loading="lazy">
  </iframe>
</div>

<div id="functional-prototype" class="section-card">
  <h2>Functional Prototype</h2>
  <h4>Purpose of the Prototype</h4>
  <p>
    The functional prototype was built to test whether a rotating fan-and-platform mechanism could move spotted lanternfly-sized objects into collection slots while maintaining smooth motion and acceptable mechanical clearance.
  </p>
  <h4>What Was Tested</h4>
  <ul>
    <li>Whether the fan moved smoothly through the bristled regions</li>
    <li>Whether the system could operate in the target low-speed range</li>
    <li>Whether friction between the fan and plate was manageable</li>
    <li>Whether bending or warping affected the mechanism</li>
    <li>Whether SLF-sized objects could actually be moved into the trap openings</li>
  </ul>
  <h4>Outcome</h4>
  <p>
    The prototype showed that the concept can move SLF-sized objects, but the wooden construction created important limitations. The fan required substantially more force to move through the bristled regions than through flat regions, indicating that the motion was not yet smooth enough. Manual cranking demonstrated that low-speed operation was possible, but motor testing was postponed. We also observed friction, bending, and spacing issues that affected reliability and capture efficiency.
  </p>
  <p>
    Based on these results, the next design iteration will likely replace wood with more precise or flexible materials, improve bristle geometry and spacing, and add better structural support such as a bearing.
  </p>
  <p>
    <a href="{{ '/assets/ODP5.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open ODP5.pdf
    </a>
  </p>
  <iframe
    src="{{ '/assets/ODP5.pdf' | relative_url }}"
    class="pdf-frame"
    loading="lazy">
  </iframe>
</div>

<div id="client-report" class="section-card">
  <h2>Client Report</h2>
  <h4>Proposed Solution</h4>
  <p>
    The final prototype is a motorized spinning trap inspired by an electronic flytrap. A bristled fan rotates around a central shaft and pushes spotted lanternflies through slots in the platform into a liquid-filled basin below. A rotating plate beneath the platform keeps all slots covered except the one directly under the fan, preventing escape. The trap is powered by a motor, so it operates without direct monitoring. It can be hung from a tree or rail via a roof hook, or freestanding via a tripod base. All structural components are 3D-printed in PLA; electronics include a DC gearbox motor, switch, and 12V battery pack.
  </p>
  <h4>How It Works</h4>
  <p>
    As the fan sweeps the platform, its bristles contain SLF from multiple sides, funneling them toward the open slot above the basin. The slot cover rotates in sync so that only one slot is open at a time — directly beneath the fan — leaving the liquid basin as the only exit path. When the client needs to empty the trap, latches on the basin allow it to be opened and cleaned.
  </p>
  <h4>Testing Results</h4>
  <ul>
    <li><strong>Capture efficiency:</strong> After one sweep of the fan, an average of 96–100% of SLF-sized objects (Swedish Fish halves) were moved into the slots across varying densities of 5–20 objects.</li>
    <li><strong>Motor torque:</strong> Required torque in all trials was well below the motor's 2.356 N·m maximum, confirming the motor is strong enough for expected operating conditions.</li>
    <li><strong>Durability:</strong> Revolution period remained consistent across 15 consecutive revolutions with no visible wear or damage.</li>
  </ul>
  <h4>Conclusion and Next Steps</h4>
  <p>
    The prototype demonstrated proof of concept and came in well under the $350 budget at $130.72. Before field deployment, three mechanical improvements are recommended: reduce bristle spacing to prevent smaller SLF from slipping through, reinforce the motor mount to eliminate shaft misalignment, and redesign for solar power to eliminate battery replacement. Future field testing should identify the most effective attractant, measure daily capture rate to size the basin appropriately, and determine the optimal fan speed based on observed SLF reaction times.
  </p>
  <p>
    <a href="{{ '/assets/O6_Exhibit_ClientReport.pdf' | relative_url }}" target="_blank" rel="noopener">
      Open Client Report PDF
    </a>
  </p>
  <iframe
    src="{{ '/assets/O6_Exhibit_ClientReport.pdf' | relative_url }}"
    class="pdf-frame"
    loading="lazy">
  </iframe>
</div>



