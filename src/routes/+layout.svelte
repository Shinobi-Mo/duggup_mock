<script>
	import '../app.pcss';
	import * as Avatar from "$lib/components/ui/avatar";
	import { Separator } from "$lib/components/ui/separator";
	import Icon from '@iconify/svelte';
	import { Button, buttonVariants } from "$lib/components/ui/button";
	import * as Dialog from "$lib/components/ui/dialog";
	import { Input } from "$lib/components/ui/input";
	import { Label } from "$lib/components/ui/label";
	import * as DropdownMenu from "$lib/components/ui/dropdown-menu";
</script>


<nav> 
	<img class="logo" src="duggup_logo.jpg" alt="logo"/>
	<h1 class="companyName" style="font-size: 18px;">duggup</h1>
	<ul class="nav">
		<li class = "Home">
			<div class="Icon_div"><Icon icon="ri:home-7-line" style="color: dark-gray"/></div>
			<div class="Text_div"><a href="/">Home</a></div>
		</li>
		<li class = "Explore">
			<div class="Icon_div"><Icon icon="clarity:timeline-line"  style="color: dark-gray" /></div>
			<div class="Text_div"><a href="/Explore">Explore</a></div>
		</li>
		<li class="Learn">
			<div class="Icon_div"><Icon icon="ion:book-outline"  style="color: dark-gray"/></div>
			<div class="Text_div"><a href="/Learn">Learn</a></div>
		</li>
		<li class="Post">
			<Dialog.Root>
				<Dialog.Trigger class={buttonVariants({ variant: "outline" })}>
					<Icon icon="fluent:add-square-48-regular"  style="color: #616161" />
					<a href="/Post">Post</a>
				</Dialog.Trigger>
				<Dialog.Content class="sm:max-w-[425px]">
					<Dialog.Header>
					<Dialog.Title>Edit profile</Dialog.Title>
					<Dialog.Description>
						Make changes to your profile here. Click save when you're done.
					</Dialog.Description>
					</Dialog.Header>
					<div class="grid gap-4 py-4">
					<div class="grid grid-cols-4 items-center gap-4">
						<Label for="name" class="text-right">Name</Label>
						<Input id="name" value="Pedro Duarte" class="col-span-3" />
					</div>
					<div class="grid grid-cols-4 items-center gap-4">
						<Label for="username" class="text-right">Username</Label>
						<Input id="username" value="@peduarte" class="col-span-3" />
					</div>
					</div>
					<Dialog.Footer>
					<Button type="submit">Save changes</Button>
					</Dialog.Footer>
				</Dialog.Content>
			</Dialog.Root>
			
		</li>
	</ul>
	<div class = "userIcon">
		  <DropdownMenu.Root>
			<DropdownMenu.Trigger asChild let:builder>
			  <Button builders={[builder]}><Avatar.Root  class="border border-black">
				<Avatar.Image src="krishna_kiran.jpeg" alt="@shadcn" />
					<Avatar.Fallback>CN</Avatar.Fallback>
			  	</Avatar.Root>
				<h3 class = "name">Krishna Kiran</h3>
				<div class = "downArrow"><Icon icon="iconamoon:arrow-down-2-light" width="20" height="20"  style="color: #616161" /></div>
			  </Button>
			</DropdownMenu.Trigger>
			<DropdownMenu.Content class="w-56">
			  <DropdownMenu.Label>My Account</DropdownMenu.Label>
			  <DropdownMenu.Separator />
			  <DropdownMenu.Group>
				<DropdownMenu.Item>
				  Profile
				</DropdownMenu.Item>
				<DropdownMenu.Item>
				  Billing
				</DropdownMenu.Item>
				<DropdownMenu.Item>
				  Settings
				</DropdownMenu.Item>
			  </DropdownMenu.Group>
			  <DropdownMenu.Separator />
			  <DropdownMenu.Item>
				Log out
			  </DropdownMenu.Item>
			</DropdownMenu.Content>
		  </DropdownMenu.Root>
	</div>

</nav>

<div class =  "seperator" ><Separator /></div>

<div class="UserDescription">
	<div class = "UserIconAndName">
		<Avatar.Root class="w-28 h-28 border-4 border-gray-90">
			<Avatar.Image src="krishna_kiran.jpeg" alt="@shadcn" />
			<Avatar.Fallback>CN</Avatar.Fallback>
		</Avatar.Root>
		<h3 class = "profileFirstName">Krishna</h3>
		<h3 class = "profileSurName">Kiran</h3>
	</div>
	<div class= "UserDescriptionDetail">
		<p>Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.</p>
		<div class="FollowButton"><Button variant="outline">Followed</Button></div>

	</div>
	<div class= "logoJobLink">
		<img class="logoRound" src="duggup_logo.jpg" alt="logo"/>
		<div class= "UserCareer">
			<h1 style="font-size: 16px;">Duggup</h1>
			<h5>CoFounder and CEO</h5>
		</div>
		<div class="UserLinks">
			<li class="MyWebsite">
				<a href="/UserWebsite">My Website</a>
				<Icon icon="quill:link-out" width="24" height="24"  style="color: #616161" />
			</li>
			
			<div class="dots"><Icon icon="tabler:dots" width="24" height="24"  style="color: #616161" /></div>
		</div>
	</div>
</div>

<div class="timeline">
	<ul>
		<li>
			<article class="card">
				<figure class="article_image">
					<img src = "STEVE JOBS.jpg" alt="article">
				</figure>
				<div class="article_content">
					<h3 class="article_heading">No amount of technology can cconvert a bad story to a good story</h3>
				</div>
			</article>
			<article class="card">
				<figure class="article_image">
					<img src = "sam.jpeg" alt="article">
				</figure>
				<div class="article_content">
					<h3 class="article_heading">Most people don't have original idea. Here is how Sam Altman pusheshimself to have ...</h3>
				</div>
			</article>
			<div  class="timeline_left">
				<span>Dec 2023</span>
			</div>	
		</li>
		<li class="JobAndCompany">
			<div class="JobCard">
				<div class="JobText">
					<h1>Co-Founder and CEO</h1>
					<h5 class="JobStatus" >Full Time <Icon icon="ph:dot" width="24" height="24"  style="color: #7d7d7d" /> Remote</h5>
				</div>
			</div>
			<div class="left">
				<img class="logoRound" src="duggup_logo.jpg" alt="logo"/>
				<div class= "UserCareer">
					<h1 style="font-size: 16px;">Duggup</h1>
					<h5 style="font-size: 12px;">San Fransisco Bay Area</h5>
					<h5 style="font-size: 12px;">Joined</h5>
					<h5 style="font-size: 12px;">Nov 2023</h5>
				</div>
			</div>
		</li>
		<li class="cardSecond">
			<article class="card">
				<figure class="article_image">
					<img src = "desktop.jpeg" alt="article">
				</figure>
				<div class="article_content">
					<h3 class="article_heading">Startup Lesson I am reflecting. Don't build for the "average person".</h3>
				</div>
			</article>
			<article class="card">
				<figure class="article_image">
					<img src = "map.png" alt="article">
				</figure>
				<div class="article_content">
					<h3 class="article_heading">Your biggest regret at 80 will be actsof omission.</h3>
				</div>
			</article>
			<div  class="timeline_left">
				<span>Oct 2023</span>
			</div>	
		</li>
		<li class="JobAndCompany">
			<div class="JobCard">
				<div class="JobText">
					<h1>VP Engineering</h1>
					<h5 class="JobStatus" >Full Time</h5>
				</div>
			</div>
			<div class="left">
				<img class="logoRound" src="better up.png" alt="logo"/>
				<div class= "UserCareer">
					<h1 style="font-size: 16px;">BetterUp</h1>
					<h5 style="font-size: 12px;">San Fransisco Bay Area</h5>
					<h5 style="font-size: 12px;">Joined</h5>
					<h5 style="font-size: 12px;">Sep 2022</h5>
				</div>
			</div>
		</li>
		
	</ul>
	
</div>
<slot />

<style>
	.companyName{
		margin-left:1px;
	}
	nav {
		display: flex;
	}
	.logo {
		margin-left: 7em;
		margin-top: 12px;
		width: 35px;
		height: 35px;
	}
	.logoRound {
		border-radius: 50%;
		margin-left: 7em;
		margin-top: 12px;
		width: 40px;
		height: 40px;
	}
	h1 {
		margin: 0;
		margin-top: 15px;
		font-weight: bold;
	}
	.nav {
		display: flex;
		margin: 0;
		margin-left: 42em;
		margin-top: 7px;
		list-style: none;
		
	}
	li.Home {
		margin-right: 20px;
		display : flex;

	}
	li.Explore {
		margin-right: 20px;
		display : flex;

	}
	li.Learn {
		margin-right: 20px;
		display : flex;

	}
	li.Post {
		margin-right: 20px;
		display : flex;

	}
	.userIcon {
		margin-top : 8px;
		margin-right : 10px;
		margin-left: 1em;
	}
	.name {
		color : black;
		margin-left : 5px;
	}
	.seperator {	
		margin-left: 100px;
		margin-top: 0.5em;
		border-top: 1px dotted  transparent;
		margin-right: 100px;
		background-image: linear-gradient(to right, rgb(50, 50, 50) 33%, rgba(255,255,255,0) 0%);
		background-position: bottom;
		background-size: 3px 1px;
		background-repeat: repeat-x;
	}
	.Icon_div {
		display: inline-block;
		margin-top: 13px;
		margin-right: 10px
	}
	.Text_div {
		display: inline-block;
		margin-top: 8px;
	}
	.UserDescription {
		display: flex
	}
	.UserIconAndName {
		margin-left: 17em;
		margin-top: 3em;
	}
	.profileFirstName {
		text-align: center;
		margin-top: 5px;
		font-weight: 700;
		font-size: large;
	}
	.profileSurName {
		text-align: center;
		font-weight: 700;
		font-size: large
	}
	.UserDescriptionDetail {
		margin-top: 4.2em;
		margin-left: 2em;
		width: 40%
	}

	.UserCareer	 {
		text-align: end;
	}
	.UserLinks  {
		margin-top: 1em;
		display: flex;
		
	}
	li.MyWebsite{
		display: flex;
	}
	.dots{
		margin-left: 1.3em;
	}
	.logoJobLink {
		margin-top: 3em;
		margin-left: 4em;
	}
	.FollowButton {
		margin-top: 2.1em;
	}
	.vertical {
            border-left: 4px dotted gray ;
            height: 90%;
            position: absolute;
            left: 21.5%;
        }
		
	.arrowUp {
			border: solid black;
			border-width: 0 100px 100px 0;
			display: inline-block;
			left: 21.5%;
			transform: rotate(-135deg);
			-webkit-transform: rotate(-135deg);
 
		}
	.article_container_right {
		margin-left: 23em;
		margin-top: 2em;
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(300px, 10em));
		gap: 40px;
	}
	.card {
		background: white;
		border-radius: 10px;
		box-shadow: 0 4px 20px 0 rgba(34,68,123,0.2);
		width: 300px;
		height: 200px;
		margin-left: 5em;
		margin-top:2em;
		}
	.article_image {
		margin: 0;
		padding: 0;
		overflow: hidden;
		height: 70%;
	}
	.article_image img {
		width :100% ;
		border-radius: 10px 10px 0 0;
	}
	.article_content   {
		font-size: 0.8em;
		padding-top: 0.9em;
		padding-bottom: 1em;
		padding-left: 1.2em;
		padding-right: 1.2em;
		font-weight: 500;
	}
	.circle {
		position: absolute;
		left: 21.5%;
		margin-right:40px;
	}
	.left_container {
		text-align: left;
	}
	.timeline ul {
		list-style: none;
		margin: 0;
		padding: 0;
		position: relative;
		left: 21.5%;
	}
	.timeline ul li{
		display: flex;
	}
	.timeline ul:before{
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 2px;
		height: 100%;
		border-left: 4px dotted #aaa;

	}
	.timeline ul li:before {
		content: '';
		width: 15px;
		height: 15px;
		border: 3px  solid rgb(0, 106, 255);
		position: absolute;
		border-radius: 100%;
		margin-top:  7.5em;
		left:-5px;	
		
	}
	.timeline ul li .timeline_left span {
		position: absolute;
	}
	.timeline ul  li .timeline_left span {
		left: -100px;
		margin-top: 7.2em;
	}
	.JobCard{
		background: white;
		box-shadow: 0 4px 20px 0 rgba(34,68,123,0.2);
		width: 680px;
		height: 80px;
		margin-left: 5em;
		margin-top:5.5em;
	}
	.JobText{
		margin-left: 2em;
		margin-top: 1.2em;
	}
	.JobStatus{
		display: flex;
		font-size: 12px;
	}
	.left{
		position: absolute;
		left: -190px;
		margin-top: 3.2em;
	}
	.cardSecond{
		margin-top: 4em;
	}
</style>


