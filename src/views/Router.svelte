<script>
import { Router, Link, Route } from "svelte-routing";

import Navbar from '../components/Navbar';
import EventTable from '../components/EventTable'
import CreateEvent from './CreateEvent';
import Dashboard from './Dashboard';
import Events from './MyEvents';
import ViewAttendance from './ViewAttendance.svelte';
import Enrolment from'./Enrolment';
import ListStudents from './ListStudents';

let url = '/';

</script>

<style>
</style>

<div class="content">
  <Router url="{url}">
    <Navbar />
    <Route path="/" component="{Dashboard}" />
    <Route path="createEvent" component="{CreateEvent}" />
    <Route path="myEvents" component="{Events}" />
    <Route path="listStudents" component="{ListStudents}" />
    <Route path="viewAttendance" component={ViewAttendance} />
    <Route path="enrol" component="{Enrolment}" />
  </Router>
</div>
