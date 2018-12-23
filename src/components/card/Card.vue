<!--
  - @copyright Copyright (c) 2018 Julius Härtl <jus@bitgrid.net>
  -
  - @author Julius Härtl <jus@bitgrid.net>
  -
  - @license GNU AGPL version 3 or any later version
  -
  - This program is free software: you can redistribute it and/or modify
  - it under the terms of the GNU Affero General Public License as
  - published by the Free Software Foundation, either version 3 of the
  - License, or (at your option) any later version.
  -
  - This program is distributed in the hope that it will be useful,
  - but WITHOUT ANY WARRANTY; without even the implied warranty of
  - MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  - GNU Affero General Public License for more details.
  -
  - You should have received a copy of the GNU Affero General Public License
  - along with this program. If not, see <http://www.gnu.org/licenses/>.
  -
  -->

<template>
	<div class="card">
		<h3>Card {{ id }}</h3>
		<ul>
			<li>labels</li>
		</ul>
		<div class="badges">
			<!-- Description -->
			<!-- Due date -->
			<!-- Comments -->
			<!-- Assigned users -->
			<div>
				<avatar uid="admin"></avatar>
			</div>
		</div>
		<popover-menu></popover-menu>
	</div>
</template>

<script>
import {Avatar, PopoverMenu} from 'nextcloud-vue'

export default {
	name: 'Card',
	components: {Avatar, PopoverMenu},
	props: {
		id: {}
	},
	computed: {
		compactMode() {
			return false
		}
	}
}
</script>

<style lang="scss" scoped>
.card {
	box-shadow: 0 0 5px #aaa;
}
</style>
