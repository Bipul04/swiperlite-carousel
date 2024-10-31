bash npm install swiperlite-carousel

   
## Usage

```javascript
/**
 * SwiperLite Carousel Documentation
 * A lightweight, performance-optimized carousel/slider
 */

// Method 1: Using HTML Data Attributes
<div class="swiperlite-container"
    data-visible-slides="1"       // Number of slides visible (can be decimal, e.g., 1.5)
    data-loop="true"              // Enable infinite loop (true/false)
    data-autoplay="true"          // Enable automatic sliding (true/false)
    data-autoplay-interval="3000" // Time between slides in milliseconds
    data-pagination="true"        // Show pagination dots (true/false)
>
    <div class="swiperlite-wrapper">
        <div class="swiperlite-track">
            <div class="swiperlite-slide">Slide 1</div>
            <div class="swiperlite-slide">Slide 2</div>
            <div class="swiperlite-slide">Slide 3</div>
        </div>
    </div>
    <button class="prev" aria-label="Previous slide">Previous</button>
    <button class="next" aria-label="Next slide">Next</button>
    <div class="swiperlite-pagination"></div>
</div>

// Method 2: Initialize all carousels on page
document.addEventListener("DOMContentLoaded", () => {
    const carousels = document.querySelectorAll('.swiperlite-container');
    carousels.forEach(container => new SwiperLite(container));
});

// Available Methods:
const carousel = new SwiperLite(container);

carousel.moveToNext();         // Move to next slide
carousel.moveToPrev();         // Move to previous slide
carousel.goToSlide(index);     // Go to specific slide (zero-based index)
carousel.pauseAutoplay();      // Pause autoplay
carousel.resumeAutoplay();     // Resume autoplay
carousel.destroy();            // Clean up and remove carousel

/**
 * Features included:
 * - Touch and mouse swipe support
 * - Keyboard navigation (arrow keys)
 * - Responsive design
 * - Accessibility features
 * - Performance optimization with requestAnimationFrame
 * - Automatic memory management
 * - Lazy loading support for images
 * - Performance monitoring
 * - Touch and mouse drag support
 * - Pause on hover/focus
 */

/**
 * Default Values:
 * - visibleSlides: 1
 * - loop: false
 * - autoplay: false
 * - autoplayInterval: 3000
 * - showPagination: false
 */

/**
 * Required HTML Structure:
 * .swiperlite-container
 *   └── .swiperlite-wrapper
 *       └── .swiperlite-track
 *           └── .swiperlite-slide
 *   └── .prev (button)
 *   └── .next (button)
 *   └── .swiperlite-pagination
 */

/**
 * For lazy loading images, use:
 * <img data-src="path/to/image.jpg" alt="Description">
 */