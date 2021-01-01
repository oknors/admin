<script>
  import { Router, Route } from "svelte-routing";

  // components for this layout
  import AdminNavbar from "components/Navbars/AdminNavbar.svelte";
  import Sidebar from "components/Sidebar/Sidebar.svelte";
  import HeaderStats from "components/Headers/HeaderStats.svelte";
  import FooterAdmin from "components/Footers/FooterAdmin.svelte";


  // pages for this layout
  import Dashboard from "views/admin/Dashboard.svelte";
  import Settings from "views/admin/Settings.svelte";
  import Maps from "views/admin/Maps.svelte";
  import ListPosts from "views/admin/ListPosts.svelte";
  import EditPost from "views/admin/EditPost.svelte";
  import CreatePost from "views/admin/CreatePost.svelte";

  export let location;
  export let admin = "";
  export let apiURL
</script>

<div>
  <Sidebar location={location} apiURL={apiURL} />
  <div class="relative md:ml-64 bg-gray-200">
    <AdminNavbar />
    <HeaderStats />
    <div class="px-4 md:px-10 mx-auto w-full -m-24">
      <Router url="admin">
        <Route path="dashboard" component="{Dashboard}" />
        <Route path="settings" component="{Settings}" />
        <Route path="maps" component="{Maps}" />
        <Route path="/:hostSlug/list" component={ListPosts} apiURL={apiURL} />
<!--        <Route path="list" component="{ListPosts}" />-->
<!--        <Route path="create" component="{CreatePost}" />-->
<!--        <Route path="edit" component="{EditPost}" />-->
      </Router>
      <FooterAdmin />
    </div>
  </div>
</div>
