<script lang="ts">
	import Particles, { type ParticlesProps } from 'svelte-particles';
	import { loadFull } from 'tsparticles';

	let particlesConfig = {
		autoPlay: true,
		background: {
			color: {
				value: '#0d47a1'
			},
			image: '',
			position: '50% 50%',
			repeat: 'no-repeat',
			size: 'cover',
			opacity: 0
		},
		fullScreen: {
			enable: true,
			zIndex: 0
		},
		detectRetina: true,
		duration: 0,
		fpsLimit: 120,
		interactivity: {
			detectsOn: 'window',
			events: {
				// onClick: {
				// 	enable: true,
				// 	mode: 'push'
				// },
				onDiv: {
					selectors: [],
					enable: false,
					mode: [],
					type: 'circle'
				},
				onHover: {
					enable: true,
					mode: 'grab'
				},
				resize: true
			},
			modes: {
				slow: {
					factor: 3,
					radius: 200
				},
				attract: {
					distance: 200,
					duration: 0.4,
					easing: 'ease-out-quad',
					factor: 1,
					maxSpeed: 50,
					speed: 1
				},
				bounce: {
					distance: 200
				},
				bubble: {
					distance: 400,
					duration: 2,
					mix: false,
					opacity: 0.8,
					size: 40,
					divs: {
						distance: 200,
						duration: 0.4,
						mix: false,
						selectors: []
					}
				},
				connect: {
					distance: 80,
					links: {
						opacity: 0.5
					},
					radius: 60
				},
				grab: {
					distance: 150,
					links: {
						blink: false,
						consent: false,
						opacity: .4
					}
				},
				push: {
					default: true,
					groups: [],
					quantity: 4
				},
				remove: {
					quantity: 2
				},
				repulse: {
					distance: 200,
					duration: 0.4,
					factor: 100,
					speed: 1,
					maxSpeed: 50,
					easing: 'ease-out-quad',
					divs: {
						distance: 200,
						duration: 0.4,
						factor: 100,
						speed: 1,
						maxSpeed: 50,
						easing: 'ease-out-quad',
						selectors: []
					}
				},
				trail: {
					delay: 1,
					pauseOnStop: false,
					quantity: 1
				},
				light: {
					area: {
						gradient: {
							start: {
								value: '#ffffff'
							},
							stop: {
								value: '#000000'
							}
						},
						radius: 1000
					},
					shadow: {
						color: {
							value: '#000000'
						},
						length: 2000
					}
				}
			}
		},
		manualParticles: [],
		motion: {
			disable: false,
			reduce: {
				factor: 4,
				value: true
			}
		},
		particles: {
			bounce: {
				horizontal: {
					random: {
						enable: false,
						minimumValue: 0.1
					},
					value: 1
				},
				vertical: {
					random: {
						enable: false,
						minimumValue: 0.1
					},
					value: 1
				}
			},
			color: {
				value: '#ffffff'
			},
			destroy: {
				mode: 'none',
				split: {
					count: 1,
					factor: {
						random: {
							enable: false,
							minimumValue: 0
						},
						value: 3
					},
					rate: {
						random: {
							enable: false,
							minimumValue: 0
						},
						value: {
							min: 4,
							max: 9
						}
					},
					sizeOffset: true
				}
			},
			groups: {},
			move: {
				angle: {
					offset: 0,
					value: 90
				},
				attract: {
					distance: 200,
					enable: false,
					rotate: {
						x: 600,
						y: 1200
					}
				},
				center: {
					x: 50,
					y: 50,
					radius: 0
				},
				decay: 0,
				distance: {},
				direction: 'none',
				drift: 0,
				enable: true,
				gravity: {
					acceleration: 9.81,
					enable: false,
					inverse: false,
					maxSpeed: 1000
				},
				path: {
					clamp: true,
					delay: {
						random: {
							enable: false,
							minimumValue: 0
						},
						value: 0
					},
					enable: false,
					options: {}
				},
				outModes: {
					default: 'out',
					bottom: 'out',
					left: 'out',
					right: 'out',
					top: 'out'
				},
				random: false,
				size: false,
				speed: 5,
				spin: {
					acceleration: 0,
					enable: false
				},
				straight: false,
				trail: {
					enable: false,
					length: 2,
					fillColor: {
						value: '#ff'
					}
				},
				vibrate: false,
				warp: false
			},
			number: {
				density: {
					enable: true,
					area: 800,
					factor: 1300
				},
				limit: 0,
				value: 100
			},
			opacity: {
				random: {
					enable: false,
					minimumValue: 0.1
				},
				value: 1,
				animation: {
					count: 0,
					enable: true,
					speed: 3,
					decay: 0,
					sync: false,
					destroy: 'none',
					startValue: 'random',
					minimumValue: 0.1
				}
			},
			reduceDuplicates: false,
			rotate: {
				random: {
					enable: false,
					minimumValue: 0
				},
				value: 0,
				animation: {
					enable: false,
					speed: 0,
					decay: 0,
					sync: false
				},
				direction: 'clockwise',
				path: false
			},
			shape: {
				options: {
					size: 0
				},
				type: 'none'
			},
			size: {
				random: {
					enable: false,
					minimumValue: 1
				},
				value: {
					min: 0.1,
					max: 10
				},
				animation: {
					count: 0,
					enable: true,
					speed: 20,
					decay: 0,
					sync: false,
					destroy: 'none',
					startValue: 'random',
					minimumValue: 0.1
				}
			},
			stroke: {
				width: 2
			},
			zIndex: {
				random: {
					enable: false,
					minimumValue: 0
				},
				value: 0,
				opacityRate: 1,
				sizeRate: 1,
				velocityRate: 1
			},
			life: {
				count: 0,
				delay: {
					random: {
						enable: false,
						minimumValue: 0
					},
					value: 0,
					sync: false
				},
				duration: {
					random: {
						enable: false,
						minimumValue: 0.0001
					},
					value: 0,
					sync: false
				}
			},
			roll: {
				darken: {
					enable: false,
					value: 0
				},
				enable: false,
				enlighten: {
					enable: false,
					value: 0
				},
				mode: 'vertical',
				speed: 25
			},
			tilt: {
				random: {
					enable: false,
					minimumValue: 0
				},
				value: 0,
				animation: {
					enable: false,
					speed: 0,
					decay: 0,
					sync: false
				},
				direction: 'clockwise',
				enable: false
			},
			wobble: {
				distance: 5,
				enable: false,
				speed: {
					angle: 50,
					move: 10
				}
			},
			links: {
				blink: false,
				color: {
					value: '#ffffff'
				},
				consent: false,
				distance: 150,
				enable: true,
				frequency: 1,
				opacity: 0.1,
				triangles: {
					enable: false,
					frequency: 1
				},
				width: 1,
				warp: false
			}
		},
		pauseOnBlur: true,
		pauseOnOutsideViewport: true,
		responsive: [],
		style: {},
		themes: [],
		zLayers: 1
	};

	let onParticlesLoaded = (event: any) => {
		const particlesContainer = event.detail.particles;

		// you can use particlesContainer to call all the Container class
		// (from the core library) methods like play, pause, refresh, start, stop
	};

	let particlesInit = async (engine: any) => {
		// you can use main to customize the tsParticles instance adding presets or custom shapes
		// this loads the tsparticles package bundle, it's the easiest method for getting everything ready
		// starting from v2 you can add only the features you need reducing the bundle size
		await loadFull(engine);
	};
</script>

<Particles
	id="tsparticles"
	options={particlesConfig}
	on:particlesLoaded={onParticlesLoaded}
	{particlesInit}
/>
