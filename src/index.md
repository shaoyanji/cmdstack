<style>    @keyframes grid {        0% { transform: translateY(-50%); }        100% { transform: translateY(0); }    }    .animate-grid {        animation: grid 15s linear infinite;    }    .synthwave-grid {        background-repeat: repeat;        background-size: 60px 60px;        height: 300vh;        inset: 0% 0px;        margin-left: -50%;        transform-origin: 100% 0 0;        width: 600vw;    }    :not(.dark) .synthwave-grid-light {        background-image:             linear-gradient(to right, rgba(0,0,0,0.6) 1px, transparent 0),            linear-gradient(to bottom, rgba(0,0,0,0.6) 1px, transparent 0);    }    .dark .synthwave-grid-dark {        background-image:             linear-gradient(to right, rgba(255,255,255,0.4) 1px, transparent 0),            linear-gradient(to bottom, rgba(255,255,255,0.4) 1px, transparent 0);    }</style><div x-data="{ angle: 60 }" class="relative dark bg-gray-900 min-h-[420px] flex flex-col items-left justify-center w-full h-full overflow-hidden border-0" x-cloak>    <h1 class="absolute w-full h-auto text-5xl font-bold text-center text-white">

# Bountystash

**╭─14:01:24 | 14 Jun, Saturday | in ─❯ cmdstack**

**╰─❯ nix build .#universe**

_**lrwxrwxrwx ... result -> /nix/store/d18hyl92g30l...-universe-1.0.0**_

</h1>        <div class="absolute inset-0 w-full h-full overflow-hidden opacity-50 pointer-events-none" style="perspective: 200px;">        <div class="absolute inset-0" :style="{ transform: `rotateX(${angle}deg)` }">            <div class="animate-grid synthwave-grid synthwave-grid-light synthwave-grid-dark"></div>        </div>        <div class="absolute bottom-0 left-0 w-full h-20 bg-gradient-to-t from-black to-transparent"></div>    </div></div>
<!-- <img src="iApztC4tnMo4oTzOjyEs.jpg"> -->
<!-- making a marquee-->
<div class="flex flex-col w-full h-full">    <div x-data x-init="            $nextTick(() => {                $refs.content.appendChild($refs.item.cloneNode(true));            });        "         class="w-full overflow-hidden text-lg italic tracking-wide text-white uppercase bg-gray-900 sm:text-xs md:text-sm lg:text-base xl:text-xl"        >        <div class="relative w-full mx-auto overflow-hidden max-w-7xl">            <div class="absolute left-0 z-20 w-40 h-full bg-gradient-to-r from-gray-900 to-transparent"></div>            <div class="absolute right-0 z-20 w-40 h-full bg-gradient-to-l from-gray-900 to-transparent"></div>            <div x-ref="content" class="flex animate-marquee">                <div x-ref="item" class="flex items-center justify-center flex-shrink-0 w-full py-2 space-x-2 container-block-02">                    <div>
    This is a
<span class="hidden sm:inline">
        Tailwind CSS and Alpine.js
</span>
    continuous marquee example
</div>
<div class="hidden sm:inline two">
        It scrolls infinitely
</div>
<div class="hidden lg:inline three">
        Without any gaps
</div>                </div>            </div>        </div>    </div>    <div x-data x-init="            $nextTick(() => {                $refs.content.appendChild($refs.item.cloneNode(true));            });        "         class="w-full overflow-hidden text-lg italic tracking-wide text-white uppercase bg-gray-900 sm:text-xs md:text-sm lg:text-base xl:text-xl"        >        <div class="relative w-full mx-auto overflow-hidden max-w-7xl">            <div class="absolute left-0 z-20 w-40 h-full bg-gradient-to-r from-gray-900 to-transparent"></div>            <div class="absolute right-0 z-20 w-40 h-full bg-gradient-to-l from-gray-900 to-transparent"></div>            <div x-ref="content" class="flex animate-marquee-reverse">                <div x-ref="item" class="flex items-center justify-center flex-shrink-0 w-full py-2 space-x-2 container-block-02">                    <div>
This is a
<span class="hidden sm:inline">
Tailwind CSS and Alpine.js
</span>
continuous marquee example
</div>                    <div class="hidden sm:inline two">
It scrolls infinitely
</div>                    <div class="hidden lg:inline three">
Without any gaps
</div>                </div>            </div>        </div>    </div></div><style>    /*     *  This is the marquee animation styles.      *  Instead of adding this CSS you may wish to implement in your tailwind config.      *  Learn more in the marquee Tailwind Config section     */    @keyframes marquee {        0% {            transform: translateX(0);        }        100% {            transform: translateX(-100%);        }    }    @keyframes marquee-reverse {        0% {            transform: translateX(-100%);        }        100% {            transform: translateX(0);        }    }    .animate-marquee {        animation: marquee 20s linear infinite;    }    .animate-marquee-reverse {        animation: marquee-reverse 20s linear infinite;    }</style><style>    /*     *  This is a container query used for the demo that does not need to be included     */    .container-block-02 {        container-type: inline-size;    }    @container (max-width: 1100px) {        .container-block-02 *:nth-child(2),        .container-block-02 *:nth-child(3) {            display: none;        }    }        @container (max-width: 1100px) {        .container-block-02 > div{            font-size:12px !important;        }    }</style>
<!-- ## Datastar Tutorial -->

<!-- <input data-bind-title /><div data-text="$title.toUpperCase()"></div><button data-on-click="@post('/endpoint')">Save</button> -->

<!-- ## AlpineJS -->

<!-- <div x-data="{ open: false }">    <button @click="open = true">Expand</button>     <span x-show="open">        Content...    </span></div> -->

<!-- ### Dropdown -->

<!-- <div x-data="{ open: false }">    <button @click="open = ! open">Toggle</button>     <div x-show="open" @click.outside="open = false"> -->

<!-- ## Does markdown -->

<!-- **work inside unsafe?** -->

<!-- </div></div> -->

### Active Search

<div    x-data="{        search: '',         items: ['foo', 'bar', 'baz'],         get filteredItems() {            return this.items.filter(                i => i.startsWith(this.search)            )        }    }">    <input x-model="search" placeholder="Search...">     <ul>        <template x-for="item in filteredItems" :key="item">            <li x-text="item"></li>        </template>    </ul></div>

<!-- ## [PinesUI](https://devdojo.com/pines/) -->

<!-- ### -->

## Introduction

There is a spectre haunting Europe today, the spectre of communism
which is manifesting itself in the form of a monopoly of the
Internet, a monopoly of the Web, and a monopoly of the
monospaced font.

<hr>

## Tables

We can use regular tables that automatically adjust to the monospace grid.
They're responsive.

<table>
<thead>
  <tr>
    <th class="width-min">Name</th>
    <th class="width-auto">Dimensions</th>
    <th class="width-min">Position</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Boboli Obelisk</td>
    <td>1.41m &times; 1.41m &times; 4.87m</td>
    <td>43°45'50.78"N 11°15'3.34"E</td>
  </tr>
  <tr>
    <td>Pyramid of Khafre</td>
    <td>215.25m &times; 215.25m &times; 136.4m</td>
    <td>29°58'34"N 31°07'51"E</td>
  </tr>
<tr>
    <td>Pyramid of Khafre</td>
    <td>215.25m &times; 215.25m &times; 136.4m</td>
    <td>29°58'34"N 31°07'51"E</td>
  </tr>
</tbody>
</table>

Note that only one column is allowed to grow.

## Forms

Here are some buttons:

<nav>
    <button>Reset</button>
    <button>Save</button>
</nav>

And inputs:

<form class="grid">
<label>First name <input type="text" placeholder="Placeholder..." /></label>
<label>Last name <input type="text" placeholder="Text goes here..." /></label>
<label>Age <input type="text" value="30" /></label>
</form>

And radio buttons:

<form class="grid">
<label><input name="radio" type="radio" /> Option #1</label>
<label><input name="radio" type="radio" /> Option #2</label>
<label><input name="radio" type="radio" /> Option #3</label>
</form>

```
╭─────────────────╮
│ MONOSPACE ROCKS │
╰─────────────────╯
```

```
┌───────┐ ┌───────┐ ┌───────┐
│Actor 1│ │Actor 2│ │Actor 3│
└───┬───┘ └───┬───┘ └───┬───┘
    │         │         │    
    │         │  msg 1  │    
    │         │────────►│    
    │         │         │    
    │  msg 2  │         │    
    │────────►│         │    
┌───┴───┐ ┌───┴───┐ ┌───┴───┐
│Actor 1│ │Actor 2│ │Actor 3│
└───────┘ └───────┘ └───────┘
```

Let's go wild and draw a chart!

```
                      Things I Have
                                              
    │                                     ████ Usable
15  │
    │                                     ░░░░ Broken
    │
12  │             ░            
    │             ░            
    │   ░         ░              
 9  │   ░         ░              
    │   ░         ░              
    │   ░         ░                    ░
 6  │   █         ░         ░          ░
    │   █         ░         ░          ░
    │   █         ░         █          ░
 3  │   █         █         █          ░
    │   █         █         █          ░
    │   █         █         █          ░
 0  └───▀─────────▀─────────▀──────────▀─────────────
      Socks     Jeans     Shirts   USB Drives
```
