<script>
import{getContext}from"svelte";import getId from"./id";import{TABS}from"./Tabs.svelte";const panel={id:getId()},{registerPanel:registerPanel,selectedPanel:selectedPanel,labeledBy:labeledBy}=getContext(TABS);registerPanel(panel);</script>
<style>.svelte-tabs__tab-panel{margin-top:.5em}</style>
<div id={panel.id} aria-labelledby={$labeledBy[panel.id]} class="svelte-tabs__tab-panel" role="tabpanel"> 
  {#if $selectedPanel===panel} <slot></slot> {/if} </div>