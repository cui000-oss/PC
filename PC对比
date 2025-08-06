<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>糯米AI vs 传统工具全面对比 - 横屏版</title>
    <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Apple Color Emoji', 'Segoe UI Emoji', 'Noto Color Emoji', sans-serif;
            overflow: hidden;
            height: 100vh;
            width: 100vw;
        }
        
        body {
            touch-action: none;
            overscroll-behavior: none;
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;

        // 图标组件
        const ChevronLeft = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 19l-7-7 7-7" />
            </svg>
        );

        const ChevronRight = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 5l7 7-7 7" />
            </svg>
        );

        const ArrowRight = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 5l7 7-7 7" />
            </svg>
        );

        const CheckCircle = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
        );

        const X = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M6 18L18 6M6 6l12 12" />
            </svg>
        );

        const Zap = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
        );

        const Video = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z" />
            </svg>
        );

        const Megaphone = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M7 4V2a1 1 0 011-1h8a1 1 0 011 1v2m-9 0h10l2 5.5V18a2 2 0 01-2 2H8a2 2 0 01-2-2V9.5L8 4z" />
            </svg>
        );

        const Share2 = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M8.684 13.342C8.886 12.938 9 12.482 9 12c0-.482-.114-.938-.316-1.342m0 2.684a3 3 0 110-2.684m0 2.684l6.632 3.316m-6.632-6l6.632-3.316m0 0a3 3 0 105.367-2.684 3 3 0 00-5.367 2.684zm0 9.316a3 3 0 105.367 2.684 3 3 0 00-5.367-2.684z" />
            </svg>
        );

        const Users = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z" />
            </svg>
        );

        const Brain = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
            </svg>
        );

        const Sparkles = ({ className }) => (
            <svg className={className} fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M5 3a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2V5a2 2 0 00-2-2H5zM5 21a2 2 0 01-2-2v-2a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H5zM19 3a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2V5a2 2 0 00-2-2h-2zM19 21a2 2 0 01-2-2v-2a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2z" />
            </svg>
        );

        const PPTDemo = () => {
            const [currentSlide, setCurrentSlide] = useState(0);

            const slides = [
                // 封面页
                {
                    type: 'cover',
                    title: '糯米AI vs 传统工具全面对比',
                    subtitle: '从单点解决到全链路智能化',
                    quote: '好的AI系统 = 10年经验的老员工\n一个眼神就心领神会，无需繁琐培训和反复沟通',
                    background: 'bg-gradient-to-br from-slate-900 via-blue-900 to-slate-800'
                },
                // 全链路闭环系统
                {
                    type: 'workflow',
                    title: '全链路闭环系统',
                    subtitle: '从公域引流到私域自动化成交的完整解决方案',
                    steps: [
                        { name: '公域引流', desc: '线上运营组+短视频编导组' },
                        { name: '内容生产', desc: '文案编导组+直播组' },
                        { name: '私域转化', desc: '私域运营组+自动化SOP' },
                        { name: '持续运营', desc: '全模块协同工作' }
                    ]
                },
                // 总结页
                {
                    type: 'summary',
                    title: '糯米AI = 替代整个部门',
                    subtitle: '一套系统，多岗位智能化替代',
                    replacements: [
                        { position: '文案岗', module: '文案编导组', icon: '✍️' },
                        { position: '剪辑岗', module: '短视频编导组', icon: '🎬' },
                        { position: '直播策划岗', module: '直播组', icon: '📺' },
                        { position: '运营岗', module: '线上运营组', icon: '📈' },
                        { position: '销售岗', module: '私域运营组', icon: '💼' }
                    ],
                    conclusion: '传统方案：多个工具 + 多个岗位 + 高成本\n糯米AI：一套系统解决全链路需求'
                },
                // 功能总览页 - 3x2网格布局
                {
                    type: 'overview',
                    title: '糯米AI五大功能模块',
                    subtitle: 'From single-point solutions to end-to-end intelligentization',
                    modules: [
                        {
                            icon: <Zap className="w-4 h-4" />,
                            name: '文案编导组 (1)',
                            subtitle: '秒出获客文案（1天1人完成3人1月工作量）',
                            keyFeatures: [
                                {
                                    title: '给主题撰写文案',
                                    desc: '输入主题、话题，1分钟生成完整钩子文案，零基础也能写出专业内容，吸引精准客户'
                                },
                                {
                                    title: '长文章改写爆款文案',
                                    desc: '粘贴长文，秒变爆款短文案，省去手动精简的繁琐过程'
                                },
                                {
                                    title: '文案润色行业爆款',
                                    desc: '导入现有文案，想法描述，瞬间提升专业度和吸引力，让平庸文案变出彩'
                                },
                                {
                                    title: '给主题生成文案（教培专用）',
                                    desc: '教培行业专用，输入主题即可快速获得精准获客文案，深度契合家长心理'
                                },
                                {
                                    title: '长文案设计师（给主题）',
                                    desc: '给个主题，自动AI展成完整长文案，结构清晰逻辑完整'
                                }
                            ]
                        },
                        {
                            icon: <Zap className="w-4 h-4" />,
                            name: '文案编导组 (2)',
                            subtitle: '更多专业文案功能',
                            keyFeatures: [
                                {
                                    title: '爆款文案跨行改写师',
                                    desc: '复制其他行业爆款文案，保持结构写作技巧，智能改写成你的行业文案内容，成功经验轻松复制'
                                },
                                {
                                    title: '爆款黄金开头（16种）',
                                    desc: '给任主题、话题，瞬间生成吸睛开头，3秒抓住用户注意力，师凝客户'
                                },
                                {
                                    title: '三点式干货文案',
                                    desc: '输入主题、话题，自动整理成三要点结构，逻辑清晰，轻松搞定，用户记忆深刻'
                                },
                                {
                                    title: '流量型文案',
                                    desc: '专门优化流量获取，快速生成高传播文案，算法友容易推荐'
                                },
                                {
                                    title: '抖红视爆款文案生成',
                                    desc: '选择平台，批量生成对应机制的流量文案，适配所有主流平台，一次创作多平台使用'
                                }
                            ]
                        },
                        {
                            icon: <Video className="w-4 h-4" />,
                            name: '短视频编导组',
                            subtitle: '短视频获客蓝海工厂（一人顶一个视频团队）',
                            keyFeatures: [
                                {
                                    title: 'AI数字人',
                                    desc: '输入文案脚本，自动生成数字人播报视频，告别真人出镜、拍摄、剪辑、画面、表现力不足等各种限制'
                                },
                                {
                                    title: '矩阵系统',
                                    desc: '智能管理多个短视频账号，统一内容发布，放大流量获取效果'
                                },
                                {
                                    title: '视频包装精剪',
                                    desc: '自动为视频添加字幕、转场、音效等包装元素，剪辑不求人'
                                }
                            ]
                        },
                        {
                            icon: <Megaphone className="w-4 h-4" />,
                            name: '直播组',
                            subtitle: '高转化直播内容生产（让直播间成交翻10倍）',
                            keyFeatures: [
                                {
                                    title: '直播稿拆解',
                                    desc: '输入竞品直播稿，智能拆解成交逻辑和话术技巧，复制成功直播间的转化密码'
                                },
                                {
                                    title: '直播稿框架',
                                    desc: '选择直播类型，自动生成完整直播稿框架，新手也能搭建专业直播流程'
                                }
                            ]
                        },
                        {
                            icon: <Share2 className="w-4 h-4" />,
                            name: '线上运营组',
                            subtitle: '全域流量获客系统（从0到1建立获客机器）',
                            keyFeatures: [
                                {
                                    title: '线上定位大师',
                                    desc: '输入行业信息，筛选找到你的差异化定位，9套定位分析，解决同质化竞争难题'
                                },
                                {
                                    title: '引流钩子设计师',
                                    desc: '根据目标客户画像，批量生成吸引精准用户的引流钩子，提升获客效率'
                                },
                                {
                                    title: '封面钩子文生图设计师',
                                    desc: '输入文案描述，自动生成高点击率的封面图片，视觉冲击力拉满'
                                },
                                {
                                    title: '封面标题生成器',
                                    desc: '结合主题内容，瞬间生成多个爆款标题选项，标题党必备神器'
                                },
                                {
                                    title: 'AI海报',
                                    desc: '输入图片信息，自动设计专业海报画面，设计0成本'
                                }
                            ]
                        },
                        {
                            icon: <Users className="w-4 h-4" />,
                            name: '私域运营组',
                            subtitle: '变现收割机（让你月业绩快速成交）',
                            keyFeatures: [
                                {
                                    title: '朋友圈大师（10种）',
                                    desc: '输入想表达的内容，生成朋友圈适用的10种不同类型的高转化朋友圈文案，覆盖日常到刺激转化的全场景，避免刷屏引起反感'
                                },
                                {
                                    title: '私域SOP策划师',
                                    desc: '私域SOP运营，制定完整的社群维护流程，详细运营人群时群转化完整链运的时间线，缓致到话术及排版'
                                },
                                {
                                    title: 'SOP补充话术',
                                    desc: '针对现有标准化流程，实现社群维护，补充时间节，以及关键节点的话术准备时期护定，提升转化效果'
                                }
                            ]
                        }
                    ]
                },
                // 文案编导组对比
                {
                    type: 'comparison',
                    title: '文案编导组对比',
                    leftSide: {
                        title: '糯米AI - 文案编导组',
                        subtitle: '秒出获客文案（1天1人完成一3人1月的工作做量）',
                        color: 'bg-orange-500',
                        features: [
                            '给主题撰写文案 - 1分钟生成完整钩子文案，零基础也能写出专业内容',
                            '长文章改写爆款 - 粘贴长文，秒变爆款短文案，省去手动精简',
                            '文案润色行业爆款 - 导入文案，瞬间提升专业度和吸引力',
                            '教培专用文案 - 输入主题即可快速获得精准获客文案',
                            '爆款黄金开头 - 16种开头，3秒抓住用户注意力',
                            '抖红视爆款文案 - 选择平台，批量生成对应机制的流量文案'
                        ],
                        advantage: '🚀 超高效率：一天一人完成3人一月的工作量，专业文案团队10年经验'
                    },
                    rightSide: {
                        title: 'DeepSeek',
                        color: 'bg-gray-500',
                        features: ['基础文案生成', '简单改写功能', '通用模板应用', '需要详细提示词', '缺乏行业针对性', '无主动交互'],
                        disadvantage: '❌ 被动生成，需要反复调试，缺乏专业理解'
                    }
                },
                // 短视频编导组对比
                {
                    type: 'comparison',
                    title: '短视频编导组对比',
                    leftSide: {
                        title: '糯米AI - 短视频编导组',
                        subtitle: '短视频获客蓝海工厂（一人顶一个视频团队）',
                        color: 'bg-orange-500',
                        features: [
                            'AI数字人 - 输入文案脚本，自动生成数字人播报视频，告别真人出镜限制',
                            '短阵系统 - 智能管理多个短视频账号，统一内容发布，放大流量获取效果',
                            '视频包装精剪 - 自动为视频添加字幕、转场、音效等包装元素，剪辑不求人'
                        ],
                        advantage: '🎬 革命性创新：无需拍摄，一键生成专业视频内容'
                    },
                    rightSide: {
                        title: '剪映',
                        color: 'bg-gray-500',
                        features: ['需要拍摄素材', '手动剪辑', '删除错误片段', '剪气口处理', '时间消耗大', '需要专业技能'],
                        disadvantage: '⏱️ 传统流程：拍摄→剪辑→修正，耗时耗力'
                    }
                },
                // 直播组对比
                {
                    type: 'comparison',
                    title: '直播组对比',
                    leftSide: {
                        title: '糯米AI - 直播组',
                        subtitle: '高转化直播内容生产（让你的直播间成交翻10倍）',
                        color: 'bg-orange-500',
                        features: [
                            '直播稿拆解 - 输入竞品直播稿，智能拆解成交逻辑和话术技巧，复制成功直播间的转化密码',
                            '直播稿框架 - 选择直播类型，自动生成完整直播稿框架，新手也能搭建专业直播流程'
                        ],
                        advantage: '🎯 深度理解直播逻辑，提供完整直播解决方案'
                    },
                    rightSide: {
                        title: '传统直播脚本工具',
                        color: 'bg-gray-500',
                        features: ['基础脚本模板', '简单话术库', '静态框架', '需要手动调整', '缺乏个性化', '无优化建议'],
                        disadvantage: '📝 只提供模板，缺乏智能化和个性化指导'
                    }
                },
                // 线上运营组对比
                {
                    type: 'comparison',
                    title: '线上运营组对比',
                    leftSide: {
                        title: '糯米AI - 线上运营组',
                        subtitle: '全域流量获客系统（从0到1建立线上获客机器）',
                        color: 'bg-orange-500',
                        features: [
                            '线上定位大师 - 输入行业信息，筛选找到差异化定位，9套定位分析',
                            '引流钩子设计师 - 批量生成吸引精准用户的引流钩子，提升获客效率',
                            '封面钩子文生图设计师 - 输入文案描述，自动生成高点击率的封面图片',
                            '封面标题生成器 - 结合主题内容，瞬间生成多个爆款标题选项',
                            'AI海报 - 输入图片信息，自动设计专业海报画面，设计0成本'
                        ],
                        advantage: '🚀 全链路运营思维，从定位到转化的完整方案'
                    },
                    rightSide: {
                        title: '单一功能工具',
                        color: 'bg-gray-500',
                        features: ['单独海报生成', '基础SOP模板', '简单素材库', '功能分散', '需要多工具协作', '缺乏整体规划'],
                        disadvantage: '🔧 功能割裂，需要多个工具拼凑，缺乏系统性'
                    }
                },
                // 私域运营对比
                {
                    type: 'comparison',
                    title: '私域运营对比',
                    leftSide: {
                        title: '糯米AI - 私域运营组',
                        subtitle: '变现收割机（让你月业绩成交）',
                        color: 'bg-orange-500',
                        features: [
                            '朋友圈大师（10种） - 生成10种不同类型的高转化朋友圈文案，覆盖全场景',
                            '私域SOP策划师 - 制定完整的社群维护流程，详细运营时间线和话术',
                            'SOP补充话术 - 针对现有流程，补充关键节点的话术准备，提升转化效果'
                        ],
                        advantage: '💬 深度理解私域运营，提供个性化运营策略'
                    },
                    rightSide: {
                        title: '朋友圈文案工具',
                        color: 'bg-gray-500',
                        features: [
                            '文案素材库',
                            '基础模板',
                            '手动提取',
                            '缺乏策略指导',
                            '无自动化'
                        ],
                        disadvantage: '📱 只提供素材，缺乏专业化运营能力'
                    }
                },
                // 结尾页面
                {
                    type: 'ending',
                    title: '运营思维升级',
                    subtitle: '糯米AI带来的不仅仅是工具升级',
                    content: '不只是工具的替换，更是企业运营思维的升级。让每个企业都能享受到AI时代的红利，实现真正的数字化转型和智能化运营。',
                    highlights: [
                        { title: '思维升级', desc: '从单点工具到全链路思维' },
                        { title: 'AI红利', desc: '享受人工智能时代的发展机遇' },
                        { title: '数字化转型', desc: '实现企业全面数字化升级' },
                        { title: '智能化运营', desc: '让AI成为企业运营的核心驱动力' }
                    ],
                    additionalContent: {
                        title: 'AI系统价值',
                        systemValue: '一套AI系统承载整个企业的运营流程，打造永动的商业引擎。',
                        management: '标准化管理，让系统更落地更实用。',
                        development: '持续优化升级中······'
                    }
                }
            ];

            const nextSlide = () => {
                setCurrentSlide((prev) => (prev + 1) % slides.length);
            };

            const prevSlide = () => {
                setCurrentSlide((prev) => (prev - 1 + slides.length) % slides.length);
            };

            const goToSlide = (index) => {
                setCurrentSlide(index);
            };

            // 键盘事件监听
            useEffect(() => {
                const handleKeyDown = (event) => {
                    if (event.key === 'ArrowLeft') {
                        event.preventDefault();
                        prevSlide();
                    } else if (event.key === 'ArrowRight') {
                        event.preventDefault();
                        nextSlide();
                    }
                };

                window.addEventListener('keydown', handleKeyDown);
                return () => {
                    window.removeEventListener('keydown', handleKeyDown);
                };
            }, []);

            // 处理屏幕点击翻页
            const handleScreenClick = (e) => {
                const rect = e.currentTarget.getBoundingClientRect();
                const clickX = e.clientX - rect.left;
                const screenWidth = rect.width;
                
                if (clickX < screenWidth / 2) {
                    prevSlide();
                } else {
                    nextSlide();
                }
            };

            // 鼠标滚轮事件处理
            const handleWheel = (e) => {
                e.preventDefault();
                if (e.deltaY > 0) {
                    nextSlide();
                } else {
                    prevSlide();
                }
            };

            const renderSlide = (slide) => {
                switch (slide.type) {
                    case 'cover':
                        return (
                            <div className={`${slide.background} text-white h-full flex flex-col justify-center items-center p-8 relative overflow-hidden`}>
                                <div className="absolute inset-0 opacity-10">
                                    <div className="absolute top-20 left-20 w-32 h-32 border border-white/20 rotate-45"></div>
                                    <div className="absolute bottom-20 right-20 w-24 h-24 border border-white/20 rotate-12"></div>
                                    <div className="absolute top-1/2 left-10 w-16 h-16 border border-white/20 rotate-45"></div>
                                </div>
                                <h1 className="text-6xl md:text-7xl font-bold text-center mb-8 relative z-10">{slide.title}</h1>
                                <p className="text-2xl md:text-3xl text-center text-blue-200 relative z-10 mb-6">{slide.subtitle}</p>
                                <div className="mt-8 text-orange-400 relative z-10 mb-8">
                                    <div className="w-20 h-1 bg-orange-400 mx-auto"></div>
                                </div>
                                {slide.quote && (
                                    <div className="relative z-10 text-center">
                                        <p className="text-lg md:text-xl text-orange-200 font-medium leading-relaxed whitespace-pre-line max-w-4xl">
                                            {slide.quote}
                                        </p>
                                    </div>
                                )}
                            </div>
                        );

                    case 'overview':
                        return (
                            <div className="bg-slate-900 text-white h-full p-2 flex flex-col">
                                <div className="text-center mb-3">
                                    <h1 className="text-2xl font-bold mb-1 text-orange-400">{slide.title}</h1>
                                    <p className="text-sm text-slate-300 tracking-wide">{slide.subtitle}</p>
                                </div>
                                
                                {/* 3x2网格布局，6个模块 */}
                                <div className="flex-1 grid grid-cols-3 grid-rows-2 gap-2 max-w-7xl mx-auto w-full">
                                    {slide.modules.map((module, index) => (
                                        <div key={index} className="bg-slate-800 rounded-lg p-2 border border-slate-700 hover:border-orange-400 transition-colors">
                                            {/* 标题区域压缩成一行 */}
                                            <div className="flex items-center justify-between mb-2 text-orange-400">
                                                <div className="flex items-center">
                                                    {module.icon}
                                                    <h3 className="text-sm font-bold ml-1">{module.name}</h3>
                                                </div>
                                            </div>
                                            {/* 副标题单独一行但字体更小 */}
                                            <p className="text-xs text-orange-300 mb-2 font-medium leading-tight">{module.subtitle}</p>
                                            
                                            <div className="space-y-1">
                                                {module.keyFeatures.map((feature, idx) => (
                                                    <div key={idx} className="bg-slate-700/30 rounded-lg p-1.5 border border-slate-600/30">
                                                        <div className="flex items-start">
                                                            <CheckCircle className="w-2.5 h-2.5 text-green-400 mr-1.5 flex-shrink-0 mt-0.5" />
                                                            <div className="flex-1">
                                                                {typeof feature === 'object' ? (
                                                                    <>
                                                                        <h4 className="text-orange-200 font-semibold text-xs mb-0.5 leading-tight">
                                                                            {feature.title}
                                                                        </h4>
                                                                        <p className="text-slate-300 text-xs leading-relaxed">
                                                                            {feature.desc}
                                                                        </p>
                                                                    </>
                                                                ) : (
                                                                    <span className="text-xs text-slate-300 leading-relaxed">{feature}</span>
                                                                )}
                                                            </div>
                                                        </div>
                                                    </div>
                                                ))}
                                            </div>
                                        </div>
                                    ))}
                                </div>
                            </div>
                        );

                    case 'ending':
                        return (
                            <div className="bg-slate-900 text-white h-full p-8 flex flex-col justify-center">
                                {/* 顶部主要内容 */}
                                <div className="text-center mb-10">
                                    <h1 className="text-5xl font-bold mb-4 text-orange-400">{slide.title}</h1>
                                    <p className="text-xl text-slate-300 mb-6">{slide.subtitle}</p>
                                    <div className="max-w-4xl mx-auto">
                                        <p className="text-lg text-orange-200 leading-relaxed">
                                            {slide.content}
                                        </p>
                                    </div>
                                </div>
                                
                                {/* 4个核心亮点 - 压缩版 */}
                                <div className="max-w-6xl mx-auto mb-10">
                                    <div className="grid grid-cols-4 gap-6">
                                        {slide.highlights.map((item, index) => (
                                            <div key={index} className="bg-slate-800 rounded-lg p-4 border border-slate-700 text-center">
                                                <h3 className="text-lg font-bold text-orange-400 mb-2">{item.title}</h3>
                                                <p className="text-slate-300 text-sm leading-relaxed">{item.desc}</p>
                                            </div>
                                        ))}
                                    </div>
                                </div>

                                {/* AI系统价值区域 - 简洁版 */}
                                <div className="max-w-5xl mx-auto mb-8">
                                    <div className="bg-slate-800 rounded-lg border-2 border-orange-400 p-6">
                                        {/* 标题部分 */}
                                        <div className="text-center mb-6">
                                            <div className="flex items-center justify-center mb-3">
                                                <Brain className="w-6 h-6 text-orange-400 mr-2" />
                                                <h3 className="text-2xl font-bold text-orange-400">{slide.additionalContent.title}</h3>
                                                <Brain className="w-6 h-6 text-orange-400 ml-2" />
                                            </div>
                                        </div>
                                        
                                        {/* 内容部分 - 垂直排列 */}
                                        <div className="text-center space-y-4">
                                            <p className="text-xl text-orange-200 font-medium leading-relaxed">
                                                {slide.additionalContent.systemValue}
                                            </p>
                                            
                                            <p className="text-lg text-blue-200 leading-relaxed">
                                                {slide.additionalContent.management}
                                            </p>
                                            
                                            <div className="flex items-center justify-center pt-2">
                                                <div className="flex items-center">
                                                    <Sparkles className="w-5 h-5 text-orange-400 mr-2 animate-pulse" />
                                                    <span className="text-orange-300 font-medium">
                                                        {slide.additionalContent.development}
                                                    </span>
                                                    <Sparkles className="w-5 h-5 text-orange-400 ml-2 animate-pulse" />
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                {/* 底部标语 */}
                                <div className="text-center">
                                    <div className="inline-flex items-center bg-gradient-to-r from-orange-500 to-blue-500 text-white px-8 py-4 rounded-lg text-2xl font-bold">
                                        <Brain className="w-8 h-8 mr-3" />
                                        AI时代，让智能成为你的竞争优势
                                        <Sparkles className="w-8 h-8 ml-3" />
                                    </div>
                                </div>
                            </div>
                        );

                    case 'workflow':
                        return (
                            <div className="bg-slate-900 text-white h-full p-6 flex flex-col justify-center">
                                <h1 className="text-4xl font-bold text-center mb-4 text-orange-400">{slide.title}</h1>
                                <p className="text-xl text-center mb-12 text-slate-300">{slide.subtitle}</p>
                                <div className="flex flex-row justify-center items-center space-x-8 max-w-6xl mx-auto">
                                    {slide.steps.map((step, index) => (
                                        <React.Fragment key={index}>
                                            <div className="bg-slate-800 rounded-lg p-6 border border-slate-700 text-center min-w-56">
                                                <div className="w-12 h-12 bg-orange-500 rounded-full flex items-center justify-center mx-auto mb-4 text-white font-bold text-lg">
                                                    {index + 1}
                                                </div>
                                                <h3 className="text-xl font-bold mb-3 text-orange-400">{step.name}</h3>
                                                <p className="text-base text-slate-300">{step.desc}</p>
                                            </div>
                                            {index < slide.steps.length - 1 && (
                                                <ArrowRight className="w-8 h-8 text-orange-400" />
                                            )}
                                        </React.Fragment>
                                    ))}
                                </div>
                                <div className="text-center mt-12">
                                    <div className="inline-block bg-orange-500 text-white px-6 py-3 rounded-lg text-xl font-bold">
                                        全链路闭环 = 系统性竞争优势
                                    </div>
                                </div>
                            </div>
                        );

                    case 'comparison':
                        return (
                            <div className="bg-slate-900 text-white h-full p-8 flex flex-col">
                                <h1 className="text-4xl font-bold text-center mb-8 text-orange-400">{slide.title}</h1>
                                <div className="flex-1 grid grid-cols-2 gap-12 max-w-7xl mx-auto">
                                    {/* 左侧 - 糯米AI */}
                                    <div className="bg-slate-800 rounded-lg p-6 border-2 border-orange-500 flex flex-col">
                                        <div className={`${slide.leftSide.color} text-white p-4 rounded-lg mb-6`}>
                                            <h2 className="text-2xl font-bold">{slide.leftSide.title}</h2>
                                            {slide.leftSide.subtitle && (
                                                <p className="text-sm text-orange-100 mt-2 font-medium">{slide.leftSide.subtitle}</p>
                                            )}
                                        </div>
                                        <div className="flex-1 space-y-4 mb-6">
                                            {slide.leftSide.features.map((feature, idx) => (
                                                <div key={idx} className="bg-slate-700/30 rounded-lg p-4 border border-slate-600/30">
                                                    <div className="flex items-start">
                                                        <CheckCircle className="w-5 h-5 text-green-400 mr-3 flex-shrink-0 mt-0.5" />
                                                        <span className="text-sm leading-relaxed text-slate-300">{feature}</span>
                                                    </div>
                                                </div>
                                            ))}
                                        </div>
                                        <div className="bg-orange-900/30 border border-orange-500 rounded-lg p-4">
                                            <p className="text-orange-300 font-medium text-sm">{slide.leftSide.advantage}</p>
                                        </div>
                                    </div>

                                    {/* 右侧 - 竞品 */}
                                    <div className="bg-slate-800 rounded-lg p-6 border-2 border-gray-500 flex flex-col">
                                        <div className={`${slide.rightSide.color} text-white p-4 rounded-lg mb-6`}>
                                            <h2 className="text-2xl font-bold">{slide.rightSide.title}</h2>
                                        </div>
                                        <div className="flex-1 space-y-4 mb-6">
                                            {slide.rightSide.features.map((feature, idx) => (
                                                <div key={idx} className="bg-slate-700/30 rounded-lg p-4 border border-slate-600/30">
                                                    <div className="flex items-center">
                                                        <X className="w-5 h-5 text-red-400 mr-3 flex-shrink-0" />
                                                        <span className="text-sm text-slate-400">{feature}</span>
                                                    </div>
                                                </div>
                                            ))}
                                        </div>
                                        <div className="bg-red-900/30 border border-red-500 rounded-lg p-4">
                                            <p className="text-red-300 font-medium text-sm">{slide.rightSide.disadvantage}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        );

                    case 'summary':
                        return (
                            <div className="bg-slate-900 text-white h-full p-8 flex flex-col justify-center">
                                <h1 className="text-5xl font-bold text-center mb-6 text-orange-400">{slide.title}</h1>
                                <p className="text-2xl text-center mb-12 text-slate-300">{slide.subtitle}</p>
                                
                                <div className="max-w-6xl mx-auto mb-12">
                                    <div className="grid grid-cols-5 gap-6">
                                        {slide.replacements.map((item, index) => (
                                            <div key={index} className="bg-slate-800 rounded-lg p-6 border border-slate-700 text-center">
                                                <div className="text-5xl mb-4">{item.icon}</div>
                                                <h3 className="text-lg font-bold text-orange-400 mb-3">{item.position}</h3>
                                                <div className="flex items-center justify-center mb-3">
                                                    <ArrowRight className="w-6 h-6 text-slate-400" />
                                                </div>
                                                <p className="text-sm text-slate-300">{item.module}</p>
                                            </div>
                                        ))}
                                    </div>
                                </div>

                                <div className="bg-gradient-to-r from-orange-900/50 to-blue-900/50 border border-orange-500 rounded-lg p-8 max-w-5xl mx-auto">
                                    <pre className="text-center text-xl leading-relaxed whitespace-pre-line text-orange-200">
                                        {slide.conclusion}
                                    </pre>
                                </div>
                            </div>
                        );

                    default:
                        return <div className="bg-slate-900 text-white h-full flex items-center justify-center">幻灯片内容</div>;
                }
            };

            return (
                <div className="w-full h-screen bg-black flex flex-col">
                    {/* PPT 内容区域 */}
                    <div 
                        className="flex-1 relative cursor-pointer" 
                        onClick={handleScreenClick}
                        onWheel={handleWheel}
                        style={{ cursor: 'pointer' }}
                    >
                        {renderSlide(slides[currentSlide])}
                        
                        {/* 翻页提示区域 */}
                        <div className="absolute left-0 top-0 w-1/2 h-full z-10 flex items-center justify-start pl-8 opacity-0 hover:opacity-100 transition-opacity">
                            <div className="bg-black/70 rounded-full p-2">
                                <ChevronLeft className="w-8 h-8 text-white" />
                            </div>
                        </div>
                        <div className="absolute right-0 top-0 w-1/2 h-full z-10 flex items-center justify-end pr-8 opacity-0 hover:opacity-100 transition-opacity">
                            <div className="bg-black/70 rounded-full p-2">
                                <ChevronRight className="w-8 h-8 text-white" />
                            </div>
                        </div>
                    </div>

                    {/* 底部控制栏 */}
                    <div className="bg-slate-800 text-white p-3 flex items-center justify-between">
                        <div className="flex items-center space-x-4">
                            <span className="text-sm">
                                {currentSlide + 1} / {slides.length}
                            </span>
                            <div className="text-sm text-slate-400">
                                糯米AI vs 传统工具对比
                            </div>
                        </div>
                        
                        {/* 幻灯片缩略图导航 */}
                        <div className="flex space-x-2">
                            {slides.map((_, index) => (
                                <button
                                    key={index}
                                    onClick={(e) => {
                                        e.stopPropagation();
                                        goToSlide(index);
                                    }}
                                    className={`w-3 h-3 rounded-full transition-colors ${
                                        index === currentSlide ? 'bg-orange-400' : 'bg-slate-600 hover:bg-slate-500'
                                    }`}
                                />
                            ))}
                        </div>
                        
                        <div className="text-sm text-slate-400">
                            ← → 键盘 / 鼠标滚轮 / 点击翻页
                        </div>
                    </div>
                </div>
            );
        };

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<PPTDemo />);
    </script>
</body>
</html>
