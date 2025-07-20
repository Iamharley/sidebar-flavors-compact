# sidebar-flavors-compact
/*
  FICHIER: assets/sidebar-flavors-compact.css
  EMPLACEMENT: /assets/sidebar-flavors-compact.css
  
  Sidebar saveurs compacte et lisible avec :
  - Dimensions réduites (320px au lieu de 380px)
  - Textes lisibles
  - Sélection nicotine intégrée
  - Scroll optimisé
*/

/* === 🎯 SIDEBAR PRINCIPALE COMPACTE === */
.flavors-sidebar {
  background: linear-gradient(135deg, #FFFEF7, #FFF8DC);
  border: 2px solid #DEB887;
  border-radius: 12px;
  padding: 20px;
  position: sticky;
  top: 20px;
  box-shadow: 0 8px 25px rgba(139, 69, 19, 0.2);
  
  /* DIMENSIONS FIXES RÉDUITES */
  width: 320px;
  max-width: 100%;
  min-height: 400px;
}

.sidebar-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 20px;
  color: #8B4513;
  text-align: center;
  text-shadow: 2px 2px 4px rgba(245, 222, 179, 0.5);
}

/* === 🎯 SÉLECTION NICOTINE COMPACTE === */
.nicotine-selection {
  background: linear-gradient(135deg, #FFF8DC, #F5DEB3);
  border: 2px solid #DEB887;
  border-radius: 8px;
  padding: 15px;
  margin-bottom: 20px;
  box-shadow: inset 0 2px 4px rgba(139, 69, 19, 0.1);
}

.nicotine-selection h3 {
  color: #8B4513;
  margin: 0 0 12px 0;
  font-size: 1rem;
  text-shadow: 1px 1px 2px rgba(245, 222, 179, 0.5);
}

.nicotine-options {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  justify-content: center;
}

.nicotine-btn {
  background: linear-gradient(135deg, #FFFEF7, #FFF8DC);
  border: 2px solid #DEB887;
  color: #8B4513;
  padding: 8px 12px;
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  text-shadow: 1px 1px 1px rgba(255,255,255,0.5);
  min-width: 45px;
  text-align: center;
  text-transform: uppercase;
}

.nicotine-btn:hover {
  border-color: #FF8E20;
  transform: translateY(-1px);
  box-shadow: 0 2px 8px rgba(255, 142, 32, 0.3);
}

.nicotine-btn.selected {
  border-color: #FF8E20;
  background: linear-gradient(135deg, #FF8E20, #D2691E);
  color: white;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
  box-shadow: 0 2px 8px rgba(255, 142, 32, 0.4);
}

.nicotine-btn:disabled {
  opacity: 0.6;
  cursor: not-allowed;
  background: #f0f0f0;
  color: #999;
}

.nicotine-info {
  margin-top: 8px;
  font-size: 0.75rem;
  color: #666;
  text-align: center;
  font-style: italic;
}

/* === 🎯 CONTAINER SCROLL FLAVORS === */
.flavors-scroll {
  max-height: 400px;
  overflow-y: auto;
  margin-bottom: 15px;
  padding-right: 8px;
}

/* === 🎯 CARDS SAVEURS COMPACTES === */
.flavor-row {
  background: linear-gradient(135deg, #FFF8DC, #F5DEB3);
  border: 1px solid #DEB887;
  border-radius: 8px;
  padding: 0;
  margin-bottom: 12px;
  cursor: pointer;
  transition: all 0.3s ease;
  overflow: hidden;
  position: relative;
}

.flavor-row:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 15px rgba(139, 69, 19, 0.15);
  border-color: #FF8E20;
}

.flavor-row.selected,
.flavor-row[data-selected="true"] {
  border: 2px solid #FF8E20;
  background: linear-gradient(135deg, #FFF8DC, #F5DEB3);
  box-shadow: 0 4px 15px rgba(255, 142, 32, 0.3);
}

.flavor-content-wrapper {
  padding: 12px;
  display: flex;
  align-items: flex-start;
  gap: 12px;
}

/* === 🎯 IMAGE SAVEUR COMPACTE === */
.flavor-image-container {
  flex-shrink: 0;
}

.flavor-thumb {
  width: 50px;
  height: 50px;
  border-radius: 6px;
  object-fit: cover;
  border: 1px solid #DEB887;
  transition: all 0.3s ease;
}

.flavor-row:hover .flavor-thumb {
  transform: scale(1.05);
  border-color: #FF8E20;
}

/* === 🎯 INFOS SAVEUR LISIBLES === */
.flavor-info {
  flex: 1;
  min-width: 0;
}

.flavor-title {
  font-size: 0.95rem;
  font-weight: 600;
  color: #8B4513;
  margin-bottom: 4px;
  text-shadow: 1px 1px 2px rgba(255,255,255,0.5);
  line-height: 1.2;
  
  /* Éviter le débordement */
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

/* === 🎯 TAGS SAVEURS === */
.flavor-tag {
  display: inline-block;
  font-size: 0.65rem;
  padding: 2px 5px;
  border-radius: 3px;
  font-weight: 600;
  margin-bottom: 6px;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
  margin-right: 4px;
}

.flavor-tag.new {
  background: linear-gradient(135deg, #8B4513, #A0522D);
  color: #F5DEB3;
}

.flavor-tag.bestseller {
  background: linear-gradient(135deg, #FF8E20, #D2691E);
  color: white;
}

/* === 🎯 DESCRIPTION SAVEUR COMPACTE === */
.flavor-desc {
  font-size: 0.75rem;
  color: #666;
  line-height: 1.3;
  margin: 0;
  
  /* Limiter à 2 lignes pour compacité */
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}

/* === 🎯 REVIEWS SECTION COMPACTE === */
.flavor-reviews {
  margin: 8px 0;
}

.reviews-summary {
  display: flex;
  align-items: center;
  gap: 6px;
  margin-bottom: 6px;
}

.rating-stars {
  font-size: 0.75rem;
}

.review-count {
  font-size: 0.7rem;
  color: #666;
}

.reviews-list {
  background: rgba(255, 255, 255, 0.8);
  border-radius: 4px;
  padding: 6px;
  margin-bottom: 6px;
  max-height: 80px;
  overflow-y: auto;
  border: 1px solid #DEB887;
  font-size: 0.7rem;
}

.review-item {
  padding: 4px 0;
  border-bottom: 1px solid #f0f0f0;
}

.review-item:last-child {
  border-bottom: none;
}

.review-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 2px;
}

.reviewer-name {
  font-size: 0.7rem;
  font-weight: 600;
  color: #8B4513;
}

.review-date {
  font-size: 0.6rem;
  color: #999;
}

.review-rating {
  font-size: 0.65rem;
  margin-bottom: 2px;
}

.review-text {
  font-size: 0.7rem;
  color: #555;
  line-height: 1.2;
  margin: 0;
  
  /* Limiter à 2 lignes */
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

/* === 🎯 BOUTON WRITE REVIEW === */
.write-review-btn {
  background: linear-gradient(135deg, #FF8E20, #D2691E);
  color: white;
  border: 1px solid #8B4513;
  padding: 4px 8px;
  border-radius: 3px;
  font-size: 0.7rem;
  cursor: pointer;
  margin-bottom: 6px;
  transition: all 0.3s ease;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
  display: block;
  width: 100%;
}

.write-review-btn:hover {
  background: linear-gradient(135deg, #D2691E, #FF8E20);
  transform: translateY(-1px);
  box-shadow: 0 2px 6px rgba(255, 142, 32, 0.3);
}

/* === 🎯 BOUTON ADD FLAVOR === */
.flavor-add-btn {
  background: linear-gradient(135deg, #FF8E20, #D2691E);
  border: 2px solid #8B4513;
  color: white;
  padding: 6px 12px;
  border-radius: 15px;
  font-size: 0.75rem;
  font-weight: 600;
  cursor: pointer;
  flex-shrink: 0;
  align-self: flex-start;
  transition: all 0.3s ease;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.flavor-add-btn:hover {
  background: linear-gradient(135deg, #D2691E, #FF8E20);
  transform: translateY(-1px);
  box-shadow: 0 2px 8px rgba(255, 142, 32, 0.4);
}

.flavor-add-btn.added {
  background: linear-gradient(135deg, #27ae60, #2ecc71);
  border-color: #1e8449;
}

/* === 🎯 SCROLL INDICATOR === */
.scroll-indicator {
  text-align: center;
  padding-top: 12px;
  border-top: 1px solid #DEB887;
}

.scroll-more {
  background: none;
  border: none;
  color: #8B4513;
  font-size: 0.85rem;
  cursor: pointer;
  text-decoration: underline;
  transition: color 0.3s ease;
  padding: 4px 8px;
}

.scroll-more:hover {
  color: #FF8E20;
  text-decoration: none;
}

/* === 🎯 SCROLLBAR STYLING === */
.flavors-scroll::-webkit-scrollbar {
  width: 4px;
}

.flavors-scroll::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 2px;
}

.flavors-scroll::-webkit-scrollbar-thumb {
  background: #DEB887;
  border-radius: 2px;
  transition: background 0.3s ease;
}

.flavors-scroll::-webkit-scrollbar-thumb:hover {
  background: #CD853F;
}

/* === 🎯 MODAL REVIEWS === */
.review-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  z-index: 999;
}

.modal-content {
  background: linear-gradient(135deg, #FFFEF7, #FFF8DC);
  padding: 30px;
  border-radius: 12px;
  max-width: 500px;
  width: 90%;
  max-height: 80vh;
  overflow-y: auto;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  border: 2px solid #DEB887;
  position: relative;
  z-index: 1001;
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.modal-header h3 {
  margin: 0;
  color: #8B4513;
  text-shadow: 1px 1px 2px rgba(245, 222, 179, 0.5);
}

.close-modal {
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #8B4513;
  padding: 0;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.close-modal:hover {
  color: #FF8E20;
  background: rgba(255, 142, 32, 0.1);
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  font-weight: 600;
  margin-bottom: 8px;
  color: #8B4513;
  font-size: 0.9rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px;
  border: 2px solid #DEB887;
  border-radius: 6px;
  font-size: 0.9rem;
  background: white;
  transition: border-color 0.3s ease;
  font-family: inherit;
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: #FF8E20;
  outline: none;
  box-shadow: 0 0 0 3px rgba(255, 142, 32, 0.1);
}

.star-rating {
  display: flex;
  gap: 5px;
  margin-bottom: 10px;
}

.star {
  cursor: pointer;
  font-size: 1.2rem;
  opacity: 0.3;
  transition: opacity 0.3s ease;
  user-select: none;
}

.star.selected,
.star:hover {
  opacity: 1;
}

.submit-review-btn {
  background: linear-gradient(135deg, #27ae60, #2ecc71);
  color: white;
  border: none;
  padding: 12px 24px;
  border-radius: 6px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  width: 100%;
  transition: all 0.3s ease;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.submit-review-btn:hover {
  background: linear-gradient(135deg, #2ecc71, #27ae60);
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(39, 174, 96, 0.3);
}

.submit-review-btn:disabled {
  opacity: 0.6;
  cursor: not-allowed;
  transform: none;
}

/* === 📱 RESPONSIVE === */
@media (max-width: 1024px) {
  .flavors-sidebar {
    width: 100%;
    position: static;
    margin-bottom: 30px;
    order: -1;
  }
  
  .flavor-content-wrapper {
    flex-direction: row;
    align-items: center;
  }
  
  .nicotine-options {
    justify-content: flex-start;
  }
}

@media (max-width: 768px) {
  .flavors-sidebar {
    padding: 15px;
  }
  
  .flavors-scroll {
    max-height: 300px;
  }
  
  .flavor-content-wrapper {
    padding: 10px;
    gap: 10px;
  }
  
  .flavor-thumb {
    width: 40px;
    height: 40px;
  }
  
  .flavor-title {
    font-size: 0.9rem;
  }
  
  .flavor-desc {
    font-size: 0.7rem;
    -webkit-line-clamp: 1;
  }
  
  .nicotine-btn {
    padding: 6px 10px;
    font-size: 0.75rem;
    min-width: 40px;
  }
  
  .modal-content {
    padding: 20px;
    margin: 20px;
  }
}

@media (max-width: 480px) {
  .flavor-title {
    font-size: 0.85rem;
  }
  
  .flavor-desc {
    display: none; /* Masquer sur très petit écran */
  }
  
  .nicotine-btn {
    padding: 5px 8px;
    font-size: 0.7rem;
    min-width: 35px;
  }
  
  .flavor-add-btn {
    padding: 5px 10px;
    font-size: 0.7rem;
  }
}

/* === 🎯 ÉTATS LOADING === */
.flavor-row.loading {
  opacity: 0.6;
  pointer-events: none;
}

.flavor-add-btn.loading {
  opacity: 0.6;
  cursor: not-allowed;
}

.flavor-add-btn.loading::after {
  content: "...";
  animation: dots 1.5s infinite;
}

@keyframes dots {
  0%, 20% { content: ""; }
  40% { content: "."; }
  60% { content: ".."; }
  80%, 100% { content: "..."; }
}
