<h1>Project Name</h1>
....



<h2>Project Description</h2>
....

<h2>My Motivation</h2>
i have a monorepo for post2video. i have there two services : web server (next.js) and worker. Each has its own githb action workflow but 90% of workflow code is the same so how to share code ?

<h2>Installation</h2>
....


<h2>Usage</h2>
....


<h2>Technologies Used</h2>
....


<h2>Design options</h2>
<ul>
    <li>`workflow_call` for Reusable Workflows</li>
    <li>Composite Actions</li>
    <li>Docker Actions</li>
    <li>Shell Scripts</li>
</ul>


<h2>workflow_call basics</h2>
<h3>Pass arguments</h3>
 define inputs in the reusable workflow 

<h3>Limitations</h3>
<ul>
    <li>
        <strong>For the Reusable Workflow (the "callee" workflow, e.g., <code>deploy-service-reusable.yml</code>):</strong>
        <ul>
            <li>You <strong>cannot</strong> have standard event triggers like <code>on: push</code>, <code>on: pull_request</code>, <code>on: schedule</code>, etc.</li>
            <li>You <strong>must</strong> have <code>on: workflow_call</code> (and optionally <code>on: workflow_dispatch</code> for manual testing).</li>
        </ul>
    </li>
    <li>
        <strong>For the Calling Workflow (the "caller" workflow, e.g., <code>nextjs-ci-cd.yml</code> or <code>worker-ci-cd.yml</code>):</strong>
        <ul>
            <li>You <strong>can</strong> have any standard event triggers (<code>on: push</code>, <code>on: pull_request</code>, <code>on: schedule</code>, etc.) or <code>on: workflow_dispatch</code>.</li>
            <li>This workflow then uses the <code>uses:</code> keyword to call the reusable workflow.</li>
        </ul>
    </li>
</ul>

<h2>Code Structure</h2>
....

<h2>Demo</h2>
....


<h2>Points of Interest</h2>
<ul>
    <li>...</li>
   
</ul>

<h2>References</h2>
<ul>
    <li><a href='https://docs.github.com/en/actions/sharing-automations/reusing-workflows'>official docs</a></li>
    <li><a href='https://www.youtube.com/watch?v=Mir-uLSQmwA'> Efficiently Run GitHub Actions Workflows Locally with act Tool </a></li>
   
</ul>

