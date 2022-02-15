<script>
	let mobileNav = { isOpen: false };

	function toggle() {
		mobileNav.isOpen = !mobileNav.isOpen;
	}
</script>

<div class="flex flex-col min-h-screen">
    <header>
        <nav class="flex justify-between p-8">
            <span class="text-2xl">MyFirstApp</span>
            <div class="hidden justify-end md:block">
                <span class="text-xl p-4">Link 1</span>
                <span class="text-xl p-4">Link 2</span>
                <span class="text-xl p-4">Link 3</span>
            </div>
            <div class="flex md:hidden" on:click={toggle}>
                <button type="button" class="text-black dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
                    <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                        <path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
                    </svg>
                </button>
            </div>
        </nav>
        {#if mobileNav.isOpen}
        <div class="flex flex-col lg:hidden text-gray-600 uppercase p-8">
            <span class="text-xl p-4">Link 1</span>
            <span class="text-xl p-4">Link 2</span>
            <span class="text-xl p-4">Link 3</span>
        </div>
    {/if}
    </header>

    <main class="flex flex-grow">
        <div class="p-8 md:w-7/12">
            
            <div class="md:text-6xl text-4xl font-bold pb-8">Hero Message: A Free Tailwind UI kit for visionary ppl.</div>
            <div class="text-xl pb-4">Content</div>
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy
            eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam
            voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita
            kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem
            ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod
            tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At
            vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd
            gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum
            dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
            invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero
            eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no
            sea takimata sanctus est Lorem ipsum dolor sit amet. Duis autem vel eum iriure
            dolor in hendrerit in vulputate velit esse molestie consequat, vel illum
            dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio
            dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te
            feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing
            elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam
            erat volutpat.
          </div>
          <div class="hidden md:block p-8 w-5/12">
        
            <div class="text-xl pb-8">
                Sidebar
            </div>

            Ut wisi enim ad minim veniam, quis nostrud exerci tation
            ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis
            autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie
            consequat.
        </div>
    </main>
    <footer class="bg-blue-400 md:flex justify-between p-8">
        <div class="pb-8 md:w-4/12">
            <span class="text-2xl">
                MyFirstApp
            </span>
            <div class="">
                A Free Tailwind UI kit for visionary applications</div>
        </div>
        <div class="pb-8">
            <div class="text-lg border-b">Main 1</div>
            <div class="">Link 1</div>
            <div class="">Link 2</div>
            <div class="">Link 3</div>
        </div> 
        <div class="pb-8">
            <div class="text-lg border-b">Main 2</div>
            <div class="">Link 1</div>
            <div class="">Link 2</div>
            <div class="">Link 3</div>
        </div>    
        <div class="pb-8">
            <div class="text-lg border-b">Main 3</div>
            <div class="">Link 1</div>
            <div class="">Link 2</div>
            <div class="">Link 3</div>
        </div>
    </footer>
</div>