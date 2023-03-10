# Install angular cli with following command
npm install -g @angular/cli

# Create new app with 
ng new my-app

# Generate new component using
ng g c test

# Types of selectors
1. dynamic component ex: <app-test></app-test>
2. classname ex: <div class="app-test"></div>
3. attribute ex: <div app-test><div>

# Use of template and styles
Use template instead of templateUrl and styles instead of styleUrls to use html and css inside ts file. Use backtick if need to use multiple lines.

# Interpolation in Angular
Using JS variables in html file using {{}}
Example: {{name}} where name is JS variable defined inside respective component class.
## NOTE: 
1. template is not aware of global js variables like window.
2. we can't perform variable assingment in interpolation

# [ngClass] directive
Helps to apply multiple css classes

# [ngStyle] directive
Helps to apply multiple css styles

# [(ngModule)] directive
Hepls to achive two way data binding
Example: <input [(ngModule)]="name" type="text" />, where name is the variable defined inside respective class component

# Structural Directives
1. ngIf
Example #01:
<h2 *ngIf="displayName; else elseBlock">
    Codevolution
</h2>
<ng-template #elseBlock>
    <h2>Hidden part</h2>
</ng-template>

Example #02:
<div *ngIf="displayName; then thenBlock; else elseBlock"></div>
<ng-template #thenBlock>
    <h3>If Part</h3>
</ng-template>

<ng-template #thenBlock>
    <h3>Else Part</h3>
</ng-template>

2. ngSwitch
Example: 
<div [ngSwitch]="color">
    <div *ngSwitchCase="'red'">You picked red color</div>
    <div *ngSwitchCase="'blue'">You picked blue color</div>
    <div *ngSwitchCase="'green'">You picked green color</div>
    <div *ngSwitchDefault>Pick Again</div>
</div>

3. ngFor
Example:
<div *ngFor="let color of colors; index as i; first as f; last as l; odd as o; even as e">
    <h3>{{i}}: {{color}} {{f}} {{l}} {{o}} {{e}}</h3>
</div>
